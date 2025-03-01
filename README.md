# Business_Analytics_Bootcamp_5

# Distrribution Charts and Plotting Basics

###Overview

This repository covers the fundamental concepts and implementation of distribution charts, including Histogram, Box Plot, Violin Plot, and Ridgeline Plot, using the Pokémon dataset. These visualizations help understand data distribution, identify outliers, and analyze patterns effectively.

Additionally, a cheatsheet for visualization customization in Matplotlib and Seaborn is provided to enhance styling and presentation.


###📊 Distribution Charts Explained

###1️⃣ Histogram

A Histogram is used to visualize the distribution of a dataset by grouping data into bins.

    * Helps in understanding the frequency distribution.
    
    * Useful for detecting skewness, peaks, and gaps.

🔹 Implementation (Seaborn & Matplotlib) with Pokémon Dataset:

    import seaborn as sns
    import matplotlib.pyplot as plt
    
    sns.histplot(df['Speed'], bins=30, kde=True, color='blue')
    plt.title('Histogram of Pokémon Speed')
    plt.show()


###2️⃣ Box Plot (Box-and-Whisker Plot)

A Box Plot displays the distribution of data based on five-number summary:

    * Minimum, Q1 (25%), Median (50%), Q3 (75%), Maximum
    
    * Detects outliers using the Interquartile Range (IQR) method.

🔹 Implementation:

    sns.boxplot(x=df['Generation'], y=df['Attack'], color='lightblue', fliersize=10)
    plt.title('Box Plot of Pokémon Attack by Generation')
    plt.show()


###3️⃣ Violin Plot

A Violin Plot combines a Box Plot and a Kernel Density Estimate (KDE) to show the data distribution.

    * Displays density variations of the dataset.
    
    * Helps in comparing multiple categories.

🔹 Implementation:

    sns.violinplot(x=df['Generation'], y=df['Total'], palette='Pastel1', linewidth=2)
    plt.title('Violin Plot of Pokémon Total Stats by Generation')
    plt.show()


###4️⃣ Ridgeline Plot

A Ridgeline Plot visualizes distributions across multiple groups.

    * Helps in comparing trends across categories.
    
    * Used in time-series or grouped data analysis.

🔹 Implementation (Using JoyPy for Ridgeline Plot):

    from joypy import joyplot
    import pandas as pd
    
    joyplot(data=df, by='Generation', column='Speed', colormap='coolwarm')
    plt.title('Ridgeline Plot of Pokémon Speed by Generation')
    plt.show()


###🔥 Key Takeaways

✔ Histogram: Shows data distribution through bins.
✔ Box Plot: Highlights outliers and quartiles.
✔ Violin Plot: Combines KDE and Box Plot for better density visualization.
✔ Ridgeline Plot: Displays multiple distributions together for comparison.


###🎨 Cheatsheet for Customization

For detailed customization options in Matplotlib and Seaborn, refer to the included cheatsheet file in the repository.

    * Adjusting colors, themes, and styles
    
    * Modifying legends, axes, and labels
    
    * Tweaking grid lines, font sizes, and transparency



###📌 References

    * Seaborn Documentation [https://seaborn.pydata.org/]
    
    * Matplotlib Documentation  [https://matplotlib.org/]
    
    * JoyPy (Ridgeline Plot) [https://github.com/leotac/joypy]


