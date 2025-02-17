### 2. A binary communication channel carries data as one of two sets of signals denoted by 0 and 1. Owing to noise, a transmitted 0 is sometimes received as a 1, and a transmitted 1 is sometimes received as a 0. For a given channel, it can be assumed that a transmitted 0 is correctly received with probability 0.95, and a transmitted 1 is correctly received with probability 0.75. Also, 70% of all messages are transmitted as a 0. If a signal is sent, determine the probability that:

1.  a 1 was received;

<!-- -->

    # Probability of transmitting

    p_t0 <- 0.7
    p_t1 <- 0.3

    # Probability of receiving

    p_r1_t0 <- 0.05 # since it is given that a transmitted 0 is correctly received with probability 0.95
    p_r1_t1 <- 0.75

    # Probability of receiving a 1

    p_r1 <- (p_r1_t0 * p_t0) + (p_r1_t1 * p_t1)
    cat("The probability of receiving a 1 or P(R=1) is", p_r1, 
        "\nor you can say that there is a", p_r1 * 100,"% chance to receive a 1.")

    ## The probability of receiving a 1 or P(R=1) is 0.26 
    ## or you can say that there is a 26 % chance to receive a 1.

1.  a 1 was transmitted given than a 1 was received.

<!-- -->

    p_t1_given_r1 <- (p_r1_t1*p_t1)/p_r1
    cat("The probability of a 1 being transmitted given that a 1 was recieved is or P(T=1|R=1) is",
        round(p_t1_given_r1, 4), 
        "\n or you can say that there is a", round(p_t1_given_r1 * 100, 2),
        "% chance that a 1 was transmitted if a 1 is received.")

    ## The probability of a 1 being transmitted given that a 1 was recieved is or P(T=1|R=1) is 0.8654 
    ##  or you can say that there is a 86.54 % chance that a 1 was transmitted if a 1 is received.

### 7. There are three employees working at an IT company: Jane, Amy, and Ava, doing 10%, 30%, and 60% of the programming, respectively. 8% of Jane’s work, 5% of Amy’s work, and just 1% of Ava‘s work is in error. What is the overall percentage of error? If a program is found with an error, who is the most likely person to have written it?

    # P(X)
    p_jane <- 0.1
    p_amy <- 0.3
    p_ava <- 0.6

    # P(E|X)
    jane_error <- 0.08
    amy_error <- 0.05
    ava_error <- 0.01

    # Calculate the total probability or the total percentage of error

    p_error <- (p_jane*jane_error) + (p_amy*amy_error) + (p_ava*ava_error)
    cat("The overall percentage of error or P(E) is", round(p_error*100,2),"%.")

    ## The overall percentage of error or P(E) is 2.9 %.

    # Individual probabilities for error using Bayes' Theorem

    jane_given_error <- (p_jane*jane_error)/p_error
    amy_given_error <- (p_amy*amy_error)/p_error
    ava_given_error <- (p_ava*ava_error)/p_error

These are the individual probabilities that these people wrote the
program given that an error occurred or P(X|E):

    cat("Jane:", round(jane_given_error*100,2), "% \nAmy:", round(amy_given_error*100,2), "% \nAva", 
        round(ava_given_error*100,2), "%")

    ## Jane: 27.59 % 
    ## Amy: 51.72 % 
    ## Ava 20.69 %

So it seems that Amy is the most likely person to have written the
program given that there is an error with a probability of 0.5172 or
51.72%.

Github Link:
<https://github.com/SylTana/APM1110-QUIJANO-JULIAN_PHILIP/tree/main/FA3>
