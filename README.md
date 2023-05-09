# QABlogPosts
Question-answering system for blog post pages from the website: improvado.io

## How does it work?

This is a Colab notebook that does web scraping on improvado.io/blog, taking most of the blog posts' titles and contents and dumping a JSON file.

After this, a pre-trained QA model created called deepset/roberta-base-squad2 is used (https://huggingface.co/deepset/roberta-base-squad2), having as inputs the titles (treated as questions) and contents to generate answers.

As one can notice, only 21 questions were generated, to validate the output.

Some of the answers are pretty straightforward, while others aren't good at all, e.g:

Question 6: How to Build an Influencer Marketing Dashboard (+ 8 metrics to track)
Answer: Marketing teams can track all essential metrics and ROI of campaigns
Question 7: The Top 7 Marketing Reporting Software Solutions for 2023
Answer: WhatagraphWhatagraph

## Next improvements

The next step is to check key metrics such as Exact Match and F1-Score to validate the model. Moreover, another step is to use the web-scrapped data to train a new QA model.




