# How can you create bar plot?

Firstly we must import ggplot2 library.

```r
library(ggplot2)
```

After that we gonna install mtcars dataset.

```r
data(mtcars)
```

Finally. We installed mtcars dataset. 

So, I wanna create hp value according to cars model. How?

```r
ggplot(mtcars, aes(x = reorder(model, hp), y = hp, fill = model)) + 
  geom_bar(stat = "identity")
```

Okey we created bar plot but the titles in this charts will be very complicated.

I will add new code to this code for this reason.

```r
ggplot(mtcars, aes(x = reorder(model, hp), y = hp, fill = model)) + 
  geom_bar(stat = "identity") +
  labs(title = "Mtcars Veri Seti: Araba Modellerine Göre HP Değeri",
       x = "Araba Modelleri",
       y = "Horsepower (HP)") +
  theme_minimal() +
  theme(axis.text.x = element_text(angle = 90, hjust = 1))
```

Finally, This code really good. 

## Description Of Code

1. **`ggplot(mtcars, aes(x = reorder(model, hp), y = hp, fill = model))`**:  
   This initializes the `ggplot2` plot.  
   - The `aes()` function defines the aesthetics of the plot.  
   - `x = reorder(model, hp)` tells the plot to order the **car models** based on the **horsepower (HP)** values in descending order.
   - `y = hp` assigns the **horsepower (HP)** values to the y-axis.
   - `fill = model` assigns a unique color to each bar based on the **car model**.

2. **`geom_bar(stat = "identity")`**:  
   This creates a bar plot.  
   - `stat = "identity"` means the height of each bar will represent the actual **horsepower (HP)** value (instead of counting occurrences).

3. **`labs(title = "Mtcars Veri Seti: Araba Modellerine Göre HP Değeri", x = "Araba Modelleri", y = "Horsepower (HP)")`**:  
   This adds the title and axis labels.  
   - `title = "Mtcars Veri Seti: Araba Modellerine Göre HP Değeri"` provides the main title of the plot.
   - `x = "Araba Modelleri"` and `y = "Horsepower (HP)"` label the x and y axes respectively.

4. **`theme_minimal()`**:  
   This applies a minimal theme to the plot, reducing unnecessary gridlines and background elements for a cleaner and more readable appearance.

5. **`theme(axis.text.x = element_text(angle = 90, hjust = 1))`**:  
   This rotates the x-axis labels (car models) by 90 degrees to prevent them from overlapping, ensuring that the text is readable. The `hjust = 1` argument aligns the text to the right.

---

# Çubuk Grafik Nasıl Oluşturulur?

Öncelikle ggplot2 kütüphanesini içe aktarmalıyız.

```r
library(ggplot2)
```

Daha sonra mtcars veri setini yükleyeceğiz.

```r
data(mtcars)
```

Sonunda mtcars veri setini yükledik.

Şimdi, araba modellerine göre hp değerini nasıl oluşturabilirim?

```r
ggplot(mtcars, aes(x = reorder(model, hp), y = hp, fill = model)) + 
  geom_bar(stat = "identity")
```

Tamam, çubuk grafiği oluşturduk ancak bu grafikteki başlıklar çok karmaşık olacak.

Bu nedenle koda yeni bir kod ekleyeceğim.

```r
ggplot(mtcars, aes(x = reorder(model, hp), y = hp, fill = model)) + 
  geom_bar(stat = "identity") +
  labs(title = "Mtcars Veri Seti: Araba Modellerine Göre HP Değeri",
       x = "Araba Modelleri",
       y = "Horsepower (HP)") +
  theme_minimal() +
  theme(axis.text.x = element_text(angle = 90, hjust = 1))
```

Sonunda, bu kod gerçekten iyi.

## Kodun Açıklaması

1. **`ggplot(mtcars, aes(x = reorder(model, hp), y = hp, fill = model))`**:  
   Bu, `ggplot2` grafiğini başlatır.  
   - `aes()` fonksiyonu, grafiğin estetik özelliklerini tanımlar.  
   - `x = reorder(model, hp)`, **araba modellerini** **beygir gücü (HP)** değerlerine göre azalan sırada sıralamayı belirtir.
   - `y = hp`, y eksenine **beygir gücü (HP)** değerlerini atar.
   - `fill = model`, her çubuğa **araba modeline** göre benzersiz bir renk atar.

2. **`geom_bar(stat = "identity")`**:  
   Bu, bir çubuk grafik oluşturur.  
   - `stat = "identity"`, her çubuğun yüksekliğinin gerçek **beygir gücü (HP)** değerini temsil edeceği anlamına gelir (oluşum sayısını saymak yerine).

3. **`labs(title = "Mtcars Veri Seti: Araba Modellerine Göre HP Değeri", x = "Araba Modelleri", y = "Horsepower (HP)")`**:  
   Bu, başlık ve eksen etiketlerini ekler.  
   - `title = "Mtcars Veri Seti: Araba Modellerine Göre HP Değeri"` grafiğin ana başlığını sağlar.
   - `x = "Araba Modelleri"` ve `y = "Horsepower (HP)"` sırasıyla x ve y eksenlerini etiketler.

4. **`theme_minimal()`**:  
   Bu, grafiğe minimal bir tema uygular, daha temiz ve daha okunabilir bir görünüm için gereksiz ızgara çizgilerini ve arka plan öğelerini azaltır.

5. **`theme(axis.text.x = element_text(angle = 90, hjust = 1))`**:  
   Bu, x ekseni etiketlerini (araba modelleri) çakışmalarını önlemek için 90 derece döndürür ve metnin okunabilir olmasını sağlar. `hjust = 1` argümanı metni sağa hizalar.



