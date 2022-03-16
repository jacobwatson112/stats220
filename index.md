# My sus meme
## This is my Meme
![](/meme.png)
## This is my Code to create my meme
```r
library(magick)

image_1 <- image_read("http://thedailycougar.com/wp-content/uploads/2020/10/PRINT_NEWS_Among-Us_Juana-Garcia.png") %>%
  image_resize("500 x 500!")

image_2 <- image_read("https://i1.sndcdn.com/artworks-Uii8SMJvNPxy8ePA-romBoQ-t500x500.jpg") %>%
  image_scale(500)

image_3 <- image_read("https://cdn.discordapp.com/attachments/947360192323026974/953504359981936740/unknown.png") %>%
  image_scale(500)

stats_text <- image_blank(width = 500, 
                          height = 500, 
                          color = "#000000") %>%
  image_annotate(text = "Among Us",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

comp_text <- image_blank(width = 500, 
                         height = 500, 
                         color = "#000000") %>%
  image_annotate(text = "Drip \n Among Us",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

ds_text <- image_blank(width = 500, 
                       height = 500, 
                       color = "#000000") %>%
  image_annotate(text = "amogus",
                 color = "#FFFFFF",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

first_row <- c(image_1, stats_text) %>%
  image_append()

second_row <- c(image_2, comp_text) %>%
  image_append()

third_row <- c(image_3, ds_text) %>%
  image_append()

meme <- c(first_row, second_row, third_row) %>%
  image_append(stack = TRUE)

meme

image_write(meme, "meme.png")
```
## My Motivations

My motivation for creating this masterpiece of a meme was the hit game Among Us.
Among us is a very relevent game which has remained in meme culture since the beginning of 2020.
The meme has evolved throughout time and I thought that I would show that evolution through the creation of my meme.  
It is also very **sus**.
