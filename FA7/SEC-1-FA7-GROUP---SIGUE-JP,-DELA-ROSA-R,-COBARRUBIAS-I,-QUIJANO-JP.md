# Time Between Student Arrivals at the FEU Library (3rd Floor) from 8:38 AM to 9:38 AM

    library(readxl)

    ## Warning: package 'readxl' was built under R version 4.4.3

    library(ggplot2)

    ## Warning: package 'ggplot2' was built under R version 4.4.3

    data = read_excel("FA7 - Data.xlsx")

    ## New names:
    ## • `` -> `...2`
    ## • `` -> `...3`
    ## • `` -> `...4`
    ## • `` -> `...5`
    ## • `` -> `...6`
    ## • `` -> `...7`

    mean = 1.1173
    lambda = 1/mean
    x = seq(0, 48, by = 1)

    pdf = dexp(x, rate = lambda)
    cdf = pexp(x, rate = lambda)

    pdf_data = data.frame(x = x, pdf = pdf)

    ggplot(pdf_data, aes(x = x, y = pdf)) +
      geom_line(color = "blue") +
      labs(title = "Probability Density Function of Exponential Distribution",
           x = "x",
           y = "Density") +
      theme_minimal()

![](SEC-1-FA7-GROUP---SIGUE-JP,-DELA-ROSA-R,-COBARRUBIAS-I,-QUIJANO-JP_files/figure-markdown_strict/unnamed-chunk-1-1.png)

    time_intervals = as.numeric(data$...5[3:50])

    ggplot(data.frame(time_intervals), aes(x = time_intervals)) + geom_histogram(binwidth = 1, fill = "blue", color = "black") + labs(title = "Histogram of Time Intervals", x = "Time Intervals", y = "Frequency") + theme_minimal()

![](SEC-1-FA7-GROUP---SIGUE-JP,-DELA-ROSA-R,-COBARRUBIAS-I,-QUIJANO-JP_files/figure-markdown_strict/unnamed-chunk-1-2.png)

## The average wait time per minute *μ* = 1.1173 and there is an expected *λ* = 0.895 student arrivals per minute.
