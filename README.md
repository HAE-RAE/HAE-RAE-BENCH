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



  
| Models            | LW | RW | SN | RC | HI | GK | Av. (w/o KGK) |
|-------------------|------------|------------|----------------------|-----------------------|---------|-------------------|---------------|
| Text-Davinci-003  | 62.2       | 62.2       | 58.7                 | 60.1                  | 30.3    | 21.4              | 49.2 (54.7)   |
| HyperClova LK-D2  | 83.1       | 82.3       | 78.0                 | 54.5                  | 81.6    | 45.1              | 70.8 (75.9)   |
| Polyglot-Ko 1.3B  | 42.0       | 41.0       | 38.6                 | 33.1                  | 48.4    | 25.6              | 38.1 (40.6)   |
| Polyglot-Ko 3.8B  | 48.5       | 42.5       | 41.8                 | 36.0                  | 58.0    | 22.7              | 41.6 (45.4)   |
| Polyglot-Ko 5.8B  | 52.1       | 51.6       | 46.4                 | 43.2                  | 67.0    | 27.8              | 48.0 (52.1)   |
| Polyglot-Ko 12.8B | 68.6       | 48.6       | 41.2                 | 40.3                  | 68.6    | 28.4              | 49.3 (53.5)   |
| KoGPT-ryan-6B     | 49.1       | 46.7       | 45.8                 | 37.4                  | 62.2    | 25.6              | 44.4 (48.2)   |
| XGLM-1.7B         | 21.3       | 22.2       | 29.4                 | 28.9                  | 17.6    | 26.1              | 24.2 (23.9)   |
| XGLM-2.9B         | 26.6       | 24.4       | 32.7                 | 32.0                  | 23.4    | 26.7              | 27.6 (27.8)   |
| XGLM-7.5B         | 37.9       | 25.7       | 41.2                 | 33.6                  | 27.7    | 26.1              | 32.0 (33.2)   |
| mT5-Base          | 36.1       | 18.8       | 22.9                 | 23.7                  | 19.1    | 25.6              | 24.4 (24.7)   |
  

<details>
<summary>Polyglot-12.8B Variants (KoAlpaca, KuLLM)</summary>
<div markdown="1">

| Models            | LW | RW | SN | RC | HI | GK | Av. (w/o KGK) |
|-------------------|------------|------------|----------------------|-----------------------|---------|-------------------|---------------|
| Polyglot-Ko 12.8B | 68.6       | 48.6       | 41.2                 | 40.3                  | 68.6    | 28.4              | 49.3 (53.5)   |
| kullm-v2 (w/o template) | 57.4 | 40.0       | 48.4                 | 38.3                  | 71.8    | 29.0              | 47.5 (51.2)   | 
| kullm-v2 (w template)   | 85.2 | 40.0       | 44.9                 | 38.7                  | 60.6    | 27.8              | 49.5 (53.9)   |  
| KoAlpaca-Polyglot-12.8B (w/o template) | 67.5 | 63.2      | 61.4   | 44.3                  | 80.3    | 30.0              | **57.8 (63.3)**   | 
 
  
  - kullm-v2 (w template) 버전에는 [prompt_no_input](https://github.com/nlpai-lab/KULLM/blob/master/templates/kullm.json) 을 사용하였습니다.

</div>
</details>

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




