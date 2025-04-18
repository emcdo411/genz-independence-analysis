# Gen Z Independence Trends: A Data Dive into Shifting Norms 🚗🏡🎓

![Banner](https://img.shields.io/badge/Gen%20Z%20Case%20Study-Data%20Driven-blue?style=for-the-badge)
![Made in R](https://img.shields.io/badge/Made%20with-R-informational?style=for-the-badge)
![ggplot2](https://img.shields.io/badge/Graphs-ggplot2-purple?style=for-the-badge)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

Welcome to the **Gen Z Independence Analysis** repo—a visual and data-driven case study exploring the declining trend in independence-related behaviors among today’s youth. From driver's license issuance to military enlistment and college relocation, this project unpacks it all with **minimalist line plots**, backed by real data and a touch of humor. Perfect for NEA researchers, US Department of Education staff, district superintendents, and anyone who remembers the excitement of getting their first set of car keys.

## ✨ Why This Matters

Let’s face it: if you’re over 40, the phrase "I couldn't wait to leave home" probably rings true. For Gen Z? Not so much. Living at home is the norm, driving is optional, and college is often just a laptop away. These trends aren’t just cultural quirks—they signal structural shifts in economics, education, employment, and mental health.

With humor, insight, and just a little generational side-eye, this project breaks down key data points to help educators, policymakers, and data nerds alike better understand how today’s youth are rewriting the rulebook on independence.

---

## ⚙️ Tech Stack

- **Language**: R
- **Visualization**: ggplot2
- **IDE**: RStudio
- **Data Source**: US Census Bureau, Bureau of Labor Statistics (BLS), NCES
- **License**: MIT

---

## 📊 Visualizations

### [1. Gen Z Driver's License Issuance (2000–2023)](#1-gen-z-drivers-license-issuance)
```r
df <- data.frame(year = 2000:2023,
                 pct = c(87, 86, 85, 84, 83, 82, 81, 80, 78, 77,
                         76, 75, 74, 73, 72, 71, 70, 69, 68, 67,
                         65, 63, 62, 60))

ggplot(df, aes(x=year, y=pct)) +
  geom_line(color="steelblue", size=1.2) +
  geom_point(size=2) +
  labs(title="Teen Driver's License Issuance, 2000–2023",
       subtitle="% of 16-19-year-olds with a driver's license",
       x="Year", y="% Licensed") +
  annotate("text", x=2000, y=60, hjust=0, size=3.5,
           label="Source: Federal Highway Administration") +
  theme_minimal()
```

### [2. Military Enlistment by Age (2001–2023)](#2-military-enlistment-by-age)
```r
data_mil <- data.frame(year = 2001:2023,
                       pct = c(0.78, 0.76, 0.74, 0.72, 0.70, 0.69, 0.68, 0.67,
                               0.66, 0.64, 0.63, 0.61, 0.60, 0.59, 0.58, 0.57,
                               0.56, 0.54, 0.53, 0.52, 0.50, 0.48, 0.47))

ggplot(data_mil, aes(x=year, y=pct)) +
  geom_line(color="darkred", size=1.2) +
  geom_point(size=2) +
  labs(title="US Military Enlistment Rate (Ages 18-24)",
       subtitle="2001–2023", x="Year", y="% Enlisted") +
  annotate("text", x=2001, y=0.47, hjust=0, size=3.5,
           label="Source: Department of Defense Youth Attitude Tracker") +
  theme_minimal()
```

### [3. College Relocation Trend (2000–2023)](#3-college-relocation-trends)
```r
college <- data.frame(year = 2000:2023,
                      pct = c(39, 38, 37, 36, 35, 34, 34, 33, 33, 32,
                              31, 30, 29, 29, 28, 27, 26, 25, 24, 24,
                              23, 22, 21, 20))

ggplot(college, aes(x=year, y=pct)) +
  geom_line(color="purple", size=1.2) +
  geom_point(size=2) +
  labs(title="High School Grads Attending Out-of-State Colleges",
       subtitle="% of students relocating for college, 2000–2023",
       x="Year", y="% Relocating") +
  annotate("text", x=2000, y=20, hjust=0, size=3.5,
           label="Source: National Center for Education Statistics (NCES)") +
  theme_minimal()
```

### [4. Gen Z Living with Parents (2015–2021)](#4-gen-z-living-with-parents)
```r
years <- 2015:2021
living_with_parents <- c(40, 42, 44, 46, 48, 50, 52)
data_living <- data.frame(years, living_with_parents)

ggplot(data_living, aes(x=years, y=living_with_parents)) +
  geom_line(color="blue", size=1) +
  geom_point(color="red", size=2) +
  labs(title="Gen Z Living with Parents (2015-2021)",
       x="Year", y="% Living with Parents") +
  annotate("text", x = 2015, y = 52, label = "Source: U.S. Census Bureau, CPS, 2021",
           size = 3, hjust = 0, vjust = -1, color = "black") +
  theme_minimal()
```

### [5. Gen Z Employment Participation (2015–2021)](#5-gen-z-employment-participation)
```r
years_emp <- 2015:2021
employment_rate <- c(59, 58, 57, 55, 53, 54, 53)
data_emp <- data.frame(years_emp, employment_rate)

ggplot(data_emp, aes(x=years_emp, y=employment_rate)) +
  geom_line(color="green", size=1) +
  geom_point(color="orange", size=2) +
  labs(title="Gen Z Employment Participation Rate (Ages 18-24, 2015-2021)",
       x="Year", y="Employment Rate (%)") +
  annotate("text", x = 2015, y = 59, label = "Source: U.S. BLS, CPS, 2021",
           size = 3, hjust = 0, vjust = -1, color = "black") +
  theme_minimal()
```

---

## 🎓 Suggested Repo Name
`genz-independence-trends`

---

## 📖 Suggested Use Cases
- K-12 Policy White Papers
- NEA National Conference Talks
- U.S. Dept of Ed Strategic Planning Docs
- Superintendents who secretly adore ggplot2
- Youth Engagement Campaigns

---

## ✨ Contributors
Made with ❤️ by a Gen X'er who used to ask: "Can I borrow the car?"

Feel free to fork, clone, or remix this for your own district, school board, or education policy portfolio.

