### 5. Overall Percentage of relevant images

    # percentage of images supplied
    p_s1 <- 0.15
    p_s2 <- 0.2
    p_s3 <- 0.25
    p_s4 <- 0.40

    # percentage of relevant images
    p_ri1 <- 0.5
    p_ri2 <- 0.6
    p_ri3 <- 0.8
    p_ri4 <- 0.85

    # total percentage
    p_t <- (p_s1*p_ri1) + (p_s2*p_ri2) + (p_s3*p_ri3) + (p_s4*p_ri4)
    cat("The total percentage of relevant images is", round(p_t*100, 2), "%.")

    ## The total percentage of relevant images is 73.5 %.

### 6. A fair coin is tossed twice.

Let E1 be the event that both tosses have the same outcome, that is,
E1=(HH, TT). Let E2 be the event that the first toss is ahead, that is,
E2=(HH, HT). Let E3 be the event that the second toss is ahead, that is,
E3=(TH, HH). Show that E1, E2, and E3 are pairwise independent but not
mutually independent.

### Let all events be S = (HH, TT, HT, TH).

E1 = (HH, TT), has a probability of 1/2 given all the events above and
since the coin is fair.

Same with both E2 = (HH, HT) and E3 = (TH, HH) which both have a
probability of 1/2, meaning all events have the same probability.

To show pairwise independence: P(E1 ∩ E2) = P(E1)P(E2), P(E2 ∩ E3) =
P(E2)P(E3), and P(E1 ∩ E3) = P(E1)P(E3)

and since P(E1 ∩ E2) = P(HH) = 1/4, as shown with S = (HH, TT, HT, TH),
P(E2 ∩ E3) = P(HH) = 1/4, P(E1 ∩ E3) = P(HH) = 1/4,

and P(E1)P(E2) = 1/2 \* 1/2 = 1/4, P(E2)P(E3) = 1/2 \* 1/2 = 1/4,
P(E1)P(E3) = 1/2 \* 1/2 = 1/4,

we can see that, indeed, P(E1 ∩ E2) = P(E1)P(E2) = 1/4, P(E2 ∩ E3) =
P(E2)P(E3) = 1/4, P(E1 ∩ E3) = P(E1)P(E3) = 1/4.

All pairwise events are equal to 1/4 and so they are proven to be
pairwise independent.

As for their mutual independence, we must show that: P(E1 ∩ E2 ∩ E3) =
P(E1)P(E2)P(E3).

P(E1 ∩ E2 ∩ E3) is P(HH) which is 1/4, so

1/4 = 1/2 \* 1/2 \* 1/2

and 1/4 ≠ 1/8.

While the events may be pairwise independent, since P(E1 ∩ E2 ∩ E3) is
not equal to P(E1)P(E2)P(E3), they are not mutually independent.

Github Link:
<https://github.com/SylTana/APM1110-QUIJANO-JULIAN_PHILIP/tree/main/FA4>
