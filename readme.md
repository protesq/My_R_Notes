
** # How can you create bar plot ? **

Firstly we must import ggplot2 library.

** library(ggplot2)**

After than we gonna install mtcars dataset.

**data(mtcars)**

Finally. We installed mtcars dataset. 

** So, I wanna create hp value according to cars model. How ?

**ggplot(mtcars, aes(x = reorder(model,hp),y=hp, fill model)) + geom_bar(stat=identity") 

Okey we created bar plot but the titles in this charts will be verys complicated.

I will add new code to this code for this reason.

** +
  labs(title = "Mtcars Veri Seti: Araba Modellerine Göre HP Değeri",
       x = "Araba Modelleri",
       y = "Horsepower (HP)") +
  theme_minimal() +
  theme(axis.text.x = element_text(angle = 90, hjust = 1))  

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

3. **`labs(title = "Mtcars Dataset: Car Models by HP Value", x = "Car Models", y = "Horsepower (HP)")`**:  
   This adds the title and axis labels.  
   - `title = "Mtcars Dataset: Car Models by HP Value"` provides the main title of the plot.
   - `x = "Car Models"` and `y = "Horsepower (HP)"` label the x and y axes respectively.

4. **`theme_minimal()`**:  
   This applies a minimal theme to the plot, reducing unnecessary gridlines and background elements for a cleaner and more readable appearance.

5. **`theme(axis.text.x = element_text(angle = 90, hjust = 1))`**:  
   This rotates the x-axis labels (car models) by 90 degrees to prevent them from overlapping, ensuring that the text is readable. The `hjust = 1` argument aligns the text to the right.



