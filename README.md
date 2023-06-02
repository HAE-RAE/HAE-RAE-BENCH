# HAE-RAE BENCH

## About HAE-RAE BENCH
HAE-RAE Bench는 언어 모델의 한국어 능력(어휘, 역사, 상식, 독해)을 평가하기 위해 제작된 벤치마크 데이터셋입니다.

## Update Logs
#### 2023.05.11
한국어 어휘, 독해, 문법, 지식 총 4가지 영역에 걸쳐 언어모델의 능력을 평가하는 벤치마크인 HAE-RAE Bench 프리뷰 공개

#### 2023.05.23
논문 작성 및 투고 

#### 2023.06.02
mT5, KULLM, Korani 벤치 마크 결과 추가.  

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

#### HAE-RAE BENCH SCORE (Ongoing)
| Models            | Loan Words | Rare Words | Standard Nomenclature | Reading Comprehension | History | General Knowledge | Av. (w/o KGK) |
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
| kullm-v2          | 57.4       | 40.0       | 48.4                 | 38.3                  | 71.8    | 29.0              | 47.5 (51.2)   |     

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

