# Extracting Sentiment and Insights from Amazon Reviews to Improve Products

### Introduction to Computer Science and Programming

Lara Filippone, Florian Goldinger

25.01.2024

## Introduction
In the ever-evolving domain of e-commerce, customer experience and feedback have become more and more significant. Recognizing the central role of these dimensions for businesses, our project aims to explore the potential of modern technology to optimize and innovate the processing of customer opinions. Specifically, we focus on Amazon product reviews, a rich source of consumer insights, although generally difficult to fully explore due to its sheer volume and unstructured nature.

The primary objective of this project is the development of an analytical tool tailored for customer service, product managers and Amazon sellers in general. The tool we propose is designed to facilitate and automate the analysis of extensive textual data from Amazon product reviews. By doing so, it empowers these stakeholders to gain instant insights on customer sentiments, experiences, and preferences, leading to informed decision-making and product enhancements.

To achieve this, we have outlined the following key functionalities for our tool:

Collection of Amazon reviews: employing web scraping techniques, the tool can gather reviews for a specific product from Amazon. This forms the foundational dataset for subsequent analyses.

Sentiment analysis: the tool performs sentiment analysis on the collected reviews, assigning a numerical score according to their positive, negative, or neutral content. This provides a quantitative measure of customer satisfaction that can be later employed for further analysis.

Keyword identification: by analyzing the review text, the tool identifies recurring keywords, highlighting the most discussed aspects of the product.

Generative AI for summarization: through the use of generative AI, the tool synthesizes the vast amount of review data into concise summaries. These summaries offer automated and quick insights into the overall customer experience.

Generative AI for product improvement suggestions: additionally, the tool uses generative AI to automatically propose actionable product improvements based on the review analysis.

User-friendly GUI: to ensure accessibility and ease of use, said functionalities are condensed within an intuitive and user-friendly graphical user interface (GUI) and accompanied by meaningful and evocative visualizations.

The expected outcome of this project is the implementation of a tool that showcases the potential of integrating various functionalities into a single platform. Although our tool is a preliminary and simple version, it is thought as a proposal for how such a system could be developed and utilized in a real-world scenario. By demonstrating the feasibility and effectiveness of combining web scraping, sentiment analysis, keyword identification, and generative AI technologies for the analysis of Amazon product reviews, this project offers insights into the practical applications of these technologies in e-commerce and customer feedback analysis.

## Code Quality and Functionality

### Code overview

Test code snippet:

``` python
product_description_div = soup.find("div", {"id": "productFactsDesktopExpander"})

    if product_description_div:
        # Check for several unordered lists betwen <ul class="a-unordered-list a-vertical a-spacing-small"> and </ul>
        unordered_lists = product_description_div.find_all("ul", {"class": "a-unordered-list"})

        if unordered_lists:
            description_text = ""

            for ul in unordered_lists:
                # Find all list items within the unordered list
                item_list = ul.find_all("li")

                if item_list:
                    # Extract text from each list item
                    list_text = "\n".join(
                       "/ " + item.find("span", {"class": "a-list-item"}).text.strip() for item in item_list
                        )

                        # Append the list text to the overall description
                        description_text += list_text

                print("version 2")
                return description_text.strip()
```

### Code functionality and quality

### Testing and bug-fixing

## Collaboration and Teamwork

### Team roles and responsibilities

### Collaboration techniques

### Conflict resolution

## Project Design and Creativity

### Innovation and creativity

### User experience

## Conclusion