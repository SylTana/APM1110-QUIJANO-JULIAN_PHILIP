## 1. Ananalogue signal received at a detector, measured in microvolts, is normally distributed with mean of 200 and variance of 256.

    curve(dnorm(x, 200, sqrt(256)), 100, 300, xlab = "Signal (microvolts)", ylab = "Density")
    grid()
    title("Normal Distribution of Analogue Signal")

![](SEC-1-FA8---QUIJANO,-JP_files/figure-markdown_strict/unnamed-chunk-1-1.png)

    cat("\n(a) What is the probability that the signal will exceed 224 microV?\n")

    ## 
    ## (a) What is the probability that the signal will exceed 224 microV?

    a = 1 - pnorm(224, 200, sqrt(256))
    cat("The probability is ", a*100, "%.\n")

    ## The probability is  6.68072 %.

    cat("\n(b) What is the probability that it will be between 186 and 224 microV?\n")

    ## 
    ## (b) What is the probability that it will be between 186 and 224 microV?

    b = pnorm(224, 200, sqrt(256)) - pnorm(186, 200, sqrt(256))
    cat("The probability is ", b*100, "%.\n")

    ## The probability is  74.24058 %.

    cat("\n(c) What is the micro voltage below which 25% of the signals will be?\n")

    ## 
    ## (c) What is the micro voltage below which 25% of the signals will be?

    c = qnorm(.25, 200, sqrt(256))
    cat("The microvoltage will be", c,".\n")

    ## The microvoltage will be 189.2082 .

    cat("\n(d) What is the probability that the signal will be less than 240 microV given that it is larger than 210 microV?\n")

    ## 
    ## (d) What is the probability that the signal will be less than 240 microV given that it is larger than 210 microV?

    d = pnorm(240, 200, sqrt(256)) - pnorm(210, 200, sqrt(256))
    cat("The probability is ", d*100, "%.\n")

    ## The probability is  25.97759 %.

    cat("\n(e) Estimate the interquartile range.\n")

    ## 
    ## (e) Estimate the interquartile range.

    e1 = qnorm(.75, 200, sqrt(256)) 
    e2 = qnorm(.25, 200, sqrt(256))
    cat("The interquartile range is (",e1,",",e2,").\n")

    ## The interquartile range is ( 210.7918 , 189.2082 ).

    cat("\n(f) What is the probability that the signal will be less than 220 microV, given that it is larger than 210 microV?\n")

    ## 
    ## (f) What is the probability that the signal will be less than 220 microV, given that it is larger than 210 microV?

    f = pnorm(220, 200, sqrt(256)) - pnorm(210, 200, sqrt(256))
    cat("The probability is ", f*100, "%.\n")

    ## The probability is  16.03358 %.

    cat("\n(g) If we know that a received signal is greater that 200 microV, what is the probability that is in fact greater than 220 microV?\n")

    ## 
    ## (g) If we know that a received signal is greater that 200 microV, what is the probability that is in fact greater than 220 microV?

    z_220 <- (220 - 200) / 16
    z_200 <- (200 - 200) / 16

    P_X_less_220 <- pnorm(z_220)
    P_X_less_200 <- pnorm(z_200)

    g <- (1 - P_X_less_220) / (1 - P_X_less_200)

    cat("The probability is ", g*100, "%.\n")

    ## The probability is  21.12995 %.

## A manufacturer of a particular type of computer system is interested in improving its customer support services. As a first step, its marketing department has been charged with the responsibility of summarizing the extent of customer problems in terms of system failures. Over a period of six months, customers were surveyed and the amount of downtime (in minutes) due to system failures they had experienced during the previous month was collected. The average downtime was found to be 25 minutes and a variance of 144. If it can be assumed that downtime is normally distributed:

    curve (dnorm(x, 25, 12), from = 0, to = 50, xlab="Downtime (minutes)", ylab="Density")
    grid()
    title("Normal Distribution of Average Downtime")

![](SEC-1-FA8---QUIJANO,-JP_files/figure-markdown_strict/unnamed-chunk-3-1.png)

1.  obtain bounds which will include 95% of the downtime of all the
    customers;

2.  obtain the bound above which 10% of the downtime is included.

<!-- -->

    cat("(a) obtain bounds which will include 95% of the downtime of all the customers;")

    ## (a) obtain bounds which will include 95% of the downtime of all the customers;

    a1 = qnorm(.025, 25, 12)
    a2 = qnorm(.975, 25, 12)
    cat("95% percent of the downtime that customers will experience will be in between", a1,  "and", a2, "minutes or [", a1,",",a2,"].\n")

    ## 95% percent of the downtime that customers will experience will be in between 1.480432 and 48.51957 minutes or [ 1.480432 , 48.51957 ].

    cat("\n(b) obtain the bound above which 10% of the downtime is included.\n")

    ## 
    ## (b) obtain the bound above which 10% of the downtime is included.

    b = qnorm(.90, 25, 12)
    cat("The bound is at ",b, "minutes.")

    ## The bound is at  40.37862 minutes.

Github Link:
<https://github.com/SylTana/APM1110-QUIJANO-JULIAN_PHILIP/tree/main/FA8>
