# HAE-TAE-Catalog

## About HAE-TAE(HAE-RAE)
"해례(HAE-RAE)"는 영어로 수집된 데이터셋을 번역하는 것에서 나아가 한국어의 고유한 특성을 반영한 Instruction Dataset을 구축하는 오픈소스 프로젝트입니다.

## v0 Models
Models trained using existing data for 3 epochs.

|               | Train Dataset   | Backbone Model   |
|---------------|-----------------|------------------|
| [haetae_v0.1.1](https://huggingface.co/GSON-backup/hae-tae-v0.1.1) | KoInstruct-Base | Polyglot-Ko 5.8B |
| [haetae_v0.1.2](https://huggingface.co/GSON-backup/hae-tae-v0.1.2) |   KoInstruct-QA | Polyglot-Ko 5.8B |
| haetae_v0.2.1 | KoInstruct-Base |        XGLM 7.5B |
| haetae_v0.2.2 |   KoInstruct-QA |        XGLM 7.5B |
| haetae_v0.3.1 | KoInstruct-Base |        Polyglot-Ko 3.8B |
| haetae_v0.3.2 |   KoInstruct-QA |        Polyglot-Ko 3.8B  |

## Current Progress
#### 2023.5 
킥 오프, 다양한 방법론을 연구 및 활용해 한국어 Instuction Dataset을 구축 시작

#### 2023.05.11
한국어 어휘, 독해, 문법, 지식 총 4가지 영역에 걸쳐 언어모델의 능력을 평가하는 벤치마크인 HAE-RAE Bench 프리뷰 공개


## HAE-RAE BENCH (Ongoing)
모든 문제는 사지선다 및 오지선다 문항으로 구성되어있습니다.

|Category       | SubCategory     | Sample Size      | Source   |
|---------------|-----------------|------------------|------------------|
|Vocabulary     | Rare Words      | 402  | 우리말겨루기|
|Vocabulary     | Loan Words      | 166  | NIKL|
|Vocabulary     | Standard Nomenclature      | 150  | NIKL|
|Knowledge      | History         | 188  |  |
|Knowledge      | Culture         | 제작 진행중  |  |
|Reading Comprehension  | Reading Comprehension | 445  | KLAT    |
|Grammatical Error Detection  | Grammatical Error Detection | 450  | NIKL    |

#### HAE-RAE BENCH SCORE (Ongoing)
|Model Name    | KLAT     |Loan Words     | Rare Words      | Standard Nomenclature   | History        |
|---------------|-----------------|------------------|------------------|------------------|------------------|
|text-davinci-003    | 60.13%     | 62.27%      | 62.18%   | 58.66%       | 30.27%      |
|HyperClova lk-d2   | 54.50%     | 83.13%      | 82.34%   | 78%       | 81.62%      |
|HyperClova lk-d     | 21.17%     | 14.37%      | 44.31%   | 12.66%       | 17.29%      |

실험에 대한 자세한 사항은 본 github repository의 HAERAE BENCH (Preview).pdf를 참고해주시길 바랍니다.

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
