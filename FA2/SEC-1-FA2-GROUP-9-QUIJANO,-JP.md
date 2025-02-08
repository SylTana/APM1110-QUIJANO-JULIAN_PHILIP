### 2. An experiment consists of tossing two fair coins. Use R to simulate this experiment 100 times and obtain the relative frequency of each possible outcome. Hence, estimate the probability of getting one head and one tail in any order.

    Coin_Toss <- sample(2, size = 100, replace = T)
    result <- table(Coin_Toss)/length(Coin_Toss)
    rounded <- round(result, 4)
    names(rounded) <- c("Head", "Tail")
    rounded

    ## Head Tail 
    ## 0.52 0.48

From a sample size of 100, heads and tails had very close relative
frequencies, it can be seen that the probability of Head vs Tail on a
fair coin is 1/2.

### 3. An experiment consists of rolling a die. Use R to simulate this experiment 600 times and obtain the relative frequency of each possible outcome. Hence, estimate the probability of getting each of 1, 2, 3, 4, 5, and 6.

    Dice_Rolls <- sample(6, size = 600, replace = T)
    result <- table(Dice_Rolls)/length(Dice_Rolls)
    rounded <- round(result, 4)
    rounded

    ## Dice_Rolls
    ##      1      2      3      4      5      6 
    ## 0.1733 0.1783 0.1400 0.1733 0.1783 0.1567

Looking at the data, it seems that, as expected, the probability of all
results from 1-6 are very close and have only small deviations with each
other. When taking their average, we get 0.1666667 which is 16.666… %
which is 1/6.

Github Link:
<https://github.com/SylTana/APM1110-QUIJANO-JULIAN_PHILIP/tree/main/FA2>
