# HAE-RAE BENCH

## About HAE-RAE BENCH
HAE-RAE Bench는 언어 모델의 한국어 능력(어휘, 역사, 상식, 독해)을 평가하기 위해 제작된 벤치마크 데이터셋입니다.

## Update Logs
#### 2023.05.11
한국어 어휘, 독해, 문법, 지식 총 4가지 영역에 걸쳐 언어모델의 능력을 평가하는 벤치마크인 HAE-RAE Bench 프리뷰 공개

#### 2023.05.23
논문 작성 및 투고 

#### 2023.06.02
mT5, KULLM, KoAlpaca 벤치 마크 결과 추가.  

## HAE-RAE BENCH (v1)
데이터셋 구성은 아래와 같습니다. 

| Category                  | Sample Size | Source |
|---------------------------|-------------|--------|
| Loan Words (LW)           | 169         | NIKL   |
| Rare Words (RW)           | 405         | -      |
| Standard Nomenclature (SN)| 153         | NIKL   |
| Reading Comprehension (RC)| 447         | KLAT   |
| General Knowledge (GK)    | 176         | -      |
| History (HI)              | 188         | -      |

#### Benchmark Results (Ongoing)

##### Evaluation Methods 

  - 3-shot: For LLMs (Text-Davinci-003 & HyperClova LK-D2) we provide three instructive examples and an initially incomplete example, with the model expected to respond with a number from one to five, indicative of its most probable answer.   
  
- log-likelihood: For the remaining models, we evaluate the probability of an instruction-answer pair for each available option in every question. The option with the highest log-likelihood indicates the most probable answer 
  
  - **Disclaimer: 3-shot is more challenging than the log-likelihood method, therefore direct comparisons between models using these different evaluation methods can be misleading.**



  
| Models            | LW | RW | SN | RC | HI | GK | Av. |
|-------------------|------------|------------|----------------------|-----------------------|---------|-------------------|---------------|
| Text-Davinci-003  | 62.2       | 62.2       | 58.7                 | 60.1                  | 30.3    | 21.4              | 49.2          |
| HyperClova LK-D2  | 83.1       | 82.3       | 78.0                 | 54.5                  | 81.6    | 45.1              | 70.8          |
| Polyglot-Ko 1.3B  | 76.33      | 48.15      | 58.82                | 34.45                 | 60.64   | 26.14             | 50.76         |
| Polyglot-Ko 3.8B  | 78.7       | 47.41      | 64.71                | 40.72                 | 69.68   | 28.41             | 54.94         |
| Polyglot-Ko 5.8B  | 82.84      | 57.04      | 67.32                | 40.72                 | 79.79   | 29.55             | 59.54         |
| Polyglot-Ko 12.8B | 87.57      | 53.33      | 61.44                | 41.61                 | 80.32   | 33.2              | 59.58         |
| UMT5-Small        | 43.79      | 23.95      | 26.80                | 23.27                 | 20.74   | 15.91             | 25.74         |
| UMT5-Base         | 50.30      | 23.21      | 25.49                | 22.82                 | 17.55   | 17.61             | 26.16         |
| UMT5-XL           | 58.58      | 25.68      | 41.83                | 24.83                 | 14.36   | 22.16             | 31.24         |
| UMT5-XXL          | 58.58      | 33.09      | 41.83                | 29.75                 | 21.81   | 21.59             | 34.44         |
  



## Contact
For any inquiry regarding evaluation, dataset, or etc please contact us at our email addresses: [spthsrbwls123@yonsei.ac.kr](spthsrbwls123@yonsei.ac.kr)

## Acknowledgement
This project is sponsored by OnelineAI(https://www.onelineai.com/)

## Contributors (가나다순)
김송성 (Benchmark Team 팀원)  
김수완 (Benchmark Team 팀원)  
김정우 (Benchmark Team 팀원)  
김휘서 (Baseline Team 팀원)  
손규진 (Benchmark Team 팀장)  
염제원 (Baseline Team 팀원)  
이재철 (Benchmark Team 팀원)  
이한울 (Baseline Team 팀장)  
정지휴 (Benchmark Team 팀원) 

## References
  
```bibtex
@misc{polyglot-ko,
  title = {{Polyglot-Ko: Open-Source Korean Autoregressive Language Model}},
  author = {Ko, Hyunwoong and Yang, Kichang and Ryu, Minho and Choi, Taekyoon and Yang, Seungmu and Hyun, jiwung and Park, Sungho},
  url = {https://www.github.com/eleutherai/polyglot},
  month = {9},
  year = {2022},
}
```

```bibtex
@misc{alpaca,
  author = {Rohan Taori and Ishaan Gulrajani and Tianyi Zhang and Yann Dubois and Xuechen Li and Carlos Guestrin and Percy Liang and Tatsunori B. Hashimoto },
  title = {Stanford Alpaca: An Instruction-following LLaMA model},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/tatsu-lab/stanford_alpaca}},
}
```

```bibtex
@misc{kullm,
  author = {NLP & AI Lab and Human-Inspired AI research},
  title = {KULLM: Korea University Large Language Model Project},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/nlpai-lab/kullm}},
}
```




