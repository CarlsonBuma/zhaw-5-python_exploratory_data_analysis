# Statistics
stats = df[['price','camera_resolution', 'battery_life', 'storage_size', 'screen_size']].describe().round(2)

    - MEAN = Average (Total / Amount)
    - STD = Standard Deviation (Spread from Mean)
        - low std => close to the mean
        - high std => vary widely from the mean

# Skewness
skew = df[['price','camera_resolution', 'battery_life', 'storage_size', 'screen_size']].skew().round(4)

    - Skewness measures the asymmetry of the distribution of data:
        - Skewness = 0: Perfectly symmetrical (like a normal distribution).
        - Positive skew: Tail is longer on the right; data is concentrated on the left.
        - Negative skew: Tail is longer on the left; data is concentrated on the right.

# Kurtosis
df[['price','rooms', 'area']].kurtosis()

    - likelihood of extreme values (outliers)
        - Normal kurtosis (Mesokurtic):
            - Tails similar to a normal distribution.
            - Kurtosis value is close to 3.
        - High kurtosis (Leptokurtic):
            - Heavy tails and a sharp peak.
            - More outliers than a normal distribution.