# TimePool: Visually Answer “Which and When” Questions On Univariate Time Series

2023 IEEE Visualization and Visual Analytics (VIS)

# Abstract and Background

- **Abstract**: Introduces TimePool, a novel visualization prototype designed to address **"which and when" questions** in **univariate** time series analysis. TimePool enables users to construct interactive queries and explore insights through visual results. It has been evaluated through example scenarios, formal user studies, and interviews with domain experts.
- **Background**: When exploring time series datasets, analysts often ask questions regarding data extremities, conditions, or comparisons with other data points. Despite extensive research, visually performing primitive analysis tasks on univariate time series remains challenging.
- **Dataset：**World Life Expectancy (WLE) dataset

# Methods

**Core Concept of TimePool**: It conducts queries at individual time steps and provides a comprehensive inspection of the "which and when" results within a familiar line graph and complementary timelines.

**Interactive Features**: Integrates multiple line charts with Gantt-like timelines, allowing interaction between different charts. A filter bar alongside enables users to interactively change query types, thresholds, and the time span of interest.

![Screenshot 2024-05-09 at 15 02 22](https://github.com/gongxinya/Reading-Notes/assets/63331601/4ca01e70-9ab7-46f2-96f0-86b0d8e76faf)
![Screenshot 2024-05-09 at 15 03 25](https://github.com/gongxinya/Reading-Notes/assets/63331601/bea992ae-0965-4c79-811b-f4bd7fa89aea)


# Visualization Encoding

- **Line and Timeline Views**: The interface includes a line chart for an overview and detailed timeline views for in-depth analysis. Each timeline represents a data case and is color-coded based on query results.
- **Dynamic Thresholds**: Users can manipulate thresholds directly on the line chart, with visual feedback updating instantly in both the line and timeline views.
- **Sorting and Filtering**: TimePool allows sorting of data cases based on query results, revealing patterns, and filtering to focus on transient or sustained patterns.

# Conclusion

TimePool has demonstrated effectiveness in performing "which and when" tasks on univariate time series data. It provides an intuitive and efficient method for time series data analysis, outperforming traditional line charts in speed and accuracy for the targeted tasks.

# Discussion

- **Advantages**: TimePool's interactive and visual approach to querying and result representation offers users a more engaging and insightful experience compared to static or less interactive methods.
- **Limitations**: While effective for "which and when" tasks on univariate time series, TimePool's applicability to multivariate time series or larger datasets may be limited and requires further development.
- **Feedback from Experts**: Domain experts rated TimePool highly for usefulness, intuitiveness, and ease of learning, suggesting its potential for application in various fields such as health informatics, educational research, and transportation engineering.
- **Future Work**: There is a need to enhance TimePool's scalability for larger datasets and to extend its capabilities to support multivariate time series visualization. Additional features suggested by experts include data input from various sources, preprocessing, annotation, reporting, and automated grouping using machine learning techniques.
