# Introduction

`ggplot2` is a powerful and versatile data visualization package in R
that allows you to create high-quality graphs and plots with ease. This
tutorial will guide you through the basics and some advanced techniques
to harness its capabilities.

<figure>
<img src="/_figures/course_image.png"
alt="Alt Text" />
<figcaption aria-hidden="true">Alt Text</figcaption>
</figure>

------------------------------------------------------------------------

# Basics of ggplot2

## Importing Required Libraries

    library(ggplot2)

    # Here’s how to create a simple scatter plot using the mpg dataset:

    ggplot(data = mpg, aes(x = displ, y = hwy)) +
      geom_point()

![](/Users/amirgolzan/GitHub/WebPageTest/_src/ggplot2_tutorial_files/figure-markdown_strict/unnamed-chunk-1-1.png)

    # Enhance your plots with themes:

    ggplot(data = mpg, aes(x = displ, y = hwy, color = class)) +
      geom_point(size = 3) +
      theme_minimal() +
      labs(title = "Fuel Efficiency by Engine Size",
           x = "Engine Displacement (L)",
           y = "Highway Miles per Gallon")

![](/Users/amirgolzan/GitHub/WebPageTest/_src/ggplot2_tutorial_files/figure-markdown_strict/unnamed-chunk-1-2.png)

    # You can also divide the plot by a categorical variable:

    ggplot(data = mpg, aes(x = displ, y = hwy)) +
      geom_point() +
      facet_wrap(~ class)

![](/Users/amirgolzan/GitHub/WebPageTest/_src/ggplot2_tutorial_files/figure-markdown_strict/unnamed-chunk-1-3.png)

    # By now, you should have a foundational understanding of ggplot2. Start experimenting with your own datasets and unlock the power of data visualization!
