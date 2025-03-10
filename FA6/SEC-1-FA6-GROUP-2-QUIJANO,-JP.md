### I. Geometric Distribution. Provide an R code for the geometric distribution. The geometric distribution is a probability distribution that models the number of trials required to achieve the first success in a sequence of Bernoulli trials, where each trial has a constant probability of success.

1.  Set the probability of success: p &lt;- 0.2

<!-- -->

    p = 0.2

1.  Generate 1000 random variables from the geometric distribution.

<!-- -->

    x = rgeom(n = 1000, prob = p)
    x

    ##    [1]  3  7 10  1  4  3  5  3  2  2 13 11  0  1  3  0  2  3  0  0  9  1  6 10
    ##   [25]  7  3  1  2  1  8  0  7  0  3  0  1 22  0  8  0  1  4  1  9  0  0  3  0
    ##   [49]  7 21  3  0  0  1  6  1  1  3  2  1  6  2 13  0  5  3  0  5  3  3  4  7
    ##   [73]  0 13  2  9  3 12  4 27  0 11  3  3  1  1  0  7  2  1  5  0  4  4 11  0
    ##   [97]  0  4  5  3  1  6  5  1  6 18  9  0  1 24  0 11  5  5  1 10  0  8  7  6
    ##  [121]  1  9  5 14  1  4 14  2  4  1  8  0  7  1  1  5  1  1  6  5  9  0  2  4
    ##  [145]  0  6 12 10  0  1  4  3  6  4 24  2  2 10  2  0  6  1  0  3  4  0  4  7
    ##  [169] 11  0  7  0  0  0  2  3  9  7  0  2  0 12  3  0  4  2  8 11  0  7  2  1
    ##  [193]  6  5  2  3  0  4  7  7  4 19  0  3  2  0  6  8 17  6 11  4  4  0  1  1
    ##  [217]  1  2  5 22  5  1  8  3  0  6  0  5 14  2  5 11  0  0  1  4  1  4  0  0
    ##  [241] 19  6  1  3  5  1  1 20  8  0  7  0  6  0  2  0  0  1  2  1  5  5  3  0
    ##  [265]  4  0  6  9  0  1  3  3  6  5  2 17  9  7  7  1  1  6  2  9  5  5  1  0
    ##  [289] 11  8  0  3 12  4  1  5 21  0  3  1  3  1 11  1  1  0  0  7  0  3 11  3
    ##  [313]  7  1  5  7  3  6 13  1  1 13  4  1  1  4  0  1  0  5 10 12  1  2  9  6
    ##  [337]  0  1  0  3  7  3  5  3  2  0 11  3  5  2  3  2  0 11  1  1 16  0  6  6
    ##  [361]  8  2  0  0  2  1  5  5  0  7  4  2  2  6  2  0  3  6  2  9 14  7  5  4
    ##  [385]  0  8 10  2  0 10  9  9  0  0  1 17  2  0  0  2  5  0  5  4 11  3  1  2
    ##  [409]  0  2  3  1 10 17 30  3  4  0  3  7  5  0  9  0  0  5  5  2  1  1 24  2
    ##  [433]  3  7 14  4  4  3  4  0  0 16  1  6  0  8 14  0  0  2  2  5  1  3 16  5
    ##  [457]  0  2  0  0  7  2 14  5  6  3  1 11  1  0  0  1  2  6  7  3  0  4  7  6
    ##  [481]  1  7  4  2  2  2  4  0  8  1  0  1  2  0  6  5  0  8  0  3  6  2  4  4
    ##  [505]  0  2  3  0  3  2  4  5  8 26  4  0  0  2 15  3  4  1  3  2 10  6 13  0
    ##  [529]  9  0 11  0  4  4  3  2  2  1 14  2  1  3  6  0 11  3  0  5  4  4  2  0
    ##  [553]  4  5  2 11  0  1  2  0  2  3  0  1  0  4  1  1  6  1  5  0  0  0  0  2
    ##  [577]  3  5  2  2 13  3  3  2  1  1  4  0  6 11  2  2  1  5  7  2 11  0  7  2
    ##  [601] 10  3  1  0  4 15  3  0  2  2  0  1 12  1  0  2  0  5  5  9  5  0 14 11
    ##  [625] 10  5 14  4  0  3  2  6  3  4  2  6  0  5  2  2  2  6  2  1  5  0  2  4
    ##  [649]  0  5  6  8  2  6  5  0 13  2  7  1  7  0  1  0  3  0  0  0  1  2  5 13
    ##  [673]  0  4  1  5  9 10  2  7  4  4  2  2  8  0  4 11  5  0  2  3 25  5  4  5
    ##  [697]  6 16  0  3  7  2  1  0  3  0  2  1  4  8  2  1  0  1  1 11  0  0  1 14
    ##  [721]  7  3  1  1  1  7  5  4  0  3  7  0  0  2  0  0 11  1  3  8  1  5  3  5
    ##  [745]  2  1  0  1  0  1  3  0 20  3  1  1  3  1  1  1  0  2  1  8  4  0  0 10
    ##  [769]  7  2  0  4  5  2  2  4  3  2  7  6  6  3  0  3  3  1  2  3 10  0  5  4
    ##  [793]  1  4  3  7  7  2  6  1  0 13  1  2  1  2  0  3  3  7  5  1  3  0  1  5
    ##  [817]  7  0  0  9  2  0  1  4  1  0  0  0  0  1  5  5  0  6  8  2  0  0  8  7
    ##  [841]  4  3  4  4  4  7  6  4  8  1  8  0  0  8 13  4  7  3  3  6  2  1 25  1
    ##  [865]  4  4  0  2  5  2  4  0  3  0  0  2  1  2 10  4 11  1  3 23  0  6 10  1
    ##  [889]  1  2 10  2  8  3  1  3  0  2  1  0  0  0  2  0  4  0  1  9  0  2  0 26
    ##  [913]  6  5  1  2  4  7  1  1  1  5  5  0  8 10  7 10  3  1  0  2  8 10  6  6
    ##  [937]  3  3  0  5 12  0  1 13  0  0  2  2  1  1  2  2  2  2  0  8  1  6  3  1
    ##  [961]  0  4  0 12  0  8  1  0  0  8  4  1  7  0  0  0  2  0  5  6  0  9  0  4
    ##  [985]  4  0  0 11 11  2  2  0  5  8 10  1  2  1  0  6

1.  Calculate some basic statistics:

<!-- -->

    mean_x = mean(x)

    var_x = var(x)

    sd_x = sd(x)

1.  Print the results in item 3 with the following output (string):

Number of trials required to achieve first success:

Mean (in 2 decimal places):

Variance (in 2 decimal places):

Standard deviation ( in 2 decimal places):

    cat("Number of trials required to achieve first success:\n" )

    ## Number of trials required to achieve first success:

    cat("Mean (in 2 decimal places):", round(mean_x, 2), "\n")

    ## Mean (in 2 decimal places): 4.02

    cat("Variance (in 2 decimal places):", round(var_x, 2), "\n")

    ## Variance (in 2 decimal places): 20.3

    cat("Standard deviation ( in 2 decimal places):", round(sd_x, 2), "\n")

    ## Standard deviation ( in 2 decimal places): 4.51

1.  Plot the histogram of the results.

<!-- -->

    hist(x, breaks = 30, main = "Geometric Distribution", 
         xlab = "Number of Trials", col = "pink")

![](SEC-1-FA6-GROUP-2-QUIJANO,-JP_files/figure-markdown_strict/unnamed-chunk-5-1.png)

### II. Hypergeometric Distribution. Consider a plant manufacturing IC chips of which 10% are expected to be defective. The chips are packed in boxes for export. Before transportation, a sample is drawn from each box. Estimate the probability that the sample contains more than 10% defectives, when:

1.  A sample of 10 is selected from a box of 40;

<!-- -->

    N = 40 # Total Population
    K = 4 # 10% expected to be defective
    n = 10  # Sample

    # We want to find P(X > 1) which is = 1 - P(X = 0) - P(X = 1), 
    # first find  P_X_0 and P_X_1

    P_X_0 = choose(K, 0) * choose(N - K, n - 0) / choose(N, n)
    P_X_0

    ## [1] 0.2998687

    P_X_1 = choose(K, 1) * choose(N - K, n - 1) / choose(N, n)
    P_X_1

    ## [1] 0.4442499

    P_X_g_1 = 1 - P_X_0 - P_X_1
    cat("The probability that a sample contains more than 10% defectives when a sample of 10 
        is selected from a box of 40 is", P_X_g_1, "or", round(100*P_X_g_1, 2), "%.")

    ## The probability that a sample contains more than 10% defectives when a sample of 10 
    ##     is selected from a box of 40 is 0.2558814 or 25.59 %.

1.  A sample of 10 is selected from a box of 5000.

<!-- -->

    # Perform the same calculations but with different values
    N = 5000 # Total Population
    K = 500 # 10% expected to be defective
    n = 10  # Sample

    # We want to find P(X > 1) which is = 1 - P(X = 0) - P(X = 1),  
    # first find  P_X_0 and P_X_1

    P_X_0 = choose(K, 0) * choose(N - K, n - 0) / choose(N, n)
    P_X_0

    ## [1] 0.3483295

    P_X_1 = choose(K, 1) * choose(N - K, n - 1) / choose(N, n)
    P_X_1

    ## [1] 0.3878084

    P_X_g_1 = 1 - P_X_0 - P_X_1
    cat("The probability that a sample contains more than 10% defectives when a sample of 10 
        is selected from a box of 40 is", P_X_g_1, "or", round(100*P_X_g_1, 2), "%.")

    ## The probability that a sample contains more than 10% defectives when a sample of 10 
    ##     is selected from a box of 40 is 0.2638622 or 26.39 %.

Github Link:
<https://github.com/SylTana/APM1110-QUIJANO-JULIAN_PHILIP/tree/main/FA6>
