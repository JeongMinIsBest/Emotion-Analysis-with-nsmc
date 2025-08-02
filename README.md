## Emotion Analysis of Movie Review from nsmc 🎥

It is a project to classify emotions of comments from Naver Movie Reviews.

- Applied TF-IDF Method and utilized Konlpy Korean Morpho Analyzer.
- Visualized the word-specific positive/negative information for verification.


## Naver Moview Review Data 🗂️

[Naver sentiment movie corpus](https://github.com/e9t/nsmc/)

This is a movie review dataset in the Korean language. Reviews were scraped from Naver Movies.
The dataset construction is based on the method noted in Large movie review dataset from Maas et al., 2011.

- All reviews are shorter than 140 characters
- Each sentiment class is sampled equally (i.e., random guess yields 50% accuracy)
  - 100K negative reviews (originally reviews of ratings 1-4)
  - 100K positive reviews (originally reviews of ratings 9-10)
  - Neutral reviews (originally reviews of ratings 5-8) are excluded


## Reference 📖

- [머신러닝_네이버 영화 리뷰 감성 분석](https://sunnyroad.tistory.com/39)
- [10-06 네이버 영화 리뷰 감성 분류하기(Naver Movie Review Sentiment Analysis)](https://wikidocs.net/44249)
