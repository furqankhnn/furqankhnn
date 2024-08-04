# Define the observed frequencies
obs_freq <- c(146, 57, 208, 89)

# Define the claimed proportions
claimed_props <- c(0.25, 0.15, 0.40, 0.20)

# Calculate the expected frequencies
expected_freq <- sum(obs_freq) * claimed_props

# Calculate the test statistic
chi2_stat <- sum((obs_freq - expected_freq)^2 / expected_freq)

# Calculate the critical value
critical_value <- qchisq(0.99, df = 4 - 1)

# Print the results
cat("Test Statistic:", chi2_stat, "\n")
cat("Critical Value:", critical_value, "\n")

if (chi2_stat > critical_value) {
  cat("Reject the null hypothesis. The observed frequencies are not consistent with the claimed proportional market share.\n")
} else {
  cat("Fail to reject the null hypothesis. The observed frequencies are consistent with the claimed proportional market share.\n")
}
<!---
furqankhnn/furqankhnn is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
