## 📚 [KSC2024 언어공학 우수논문]**명확화 질문을 통한 모호한 객체 참조 해결과 시각적 질의 응답 성능 향상**

### 🌟 **개요**  
본 레포지토리는 **시각적 질의 응답(VQA)** 작업에서 발생하는 **모호한 객체 참조 문제**를 해결하기 위해 **명확화 질문 생성** 방식을 제안하고 이를 통해 **VQA 성능 향상**을 입증하는 코드와 실험 결과를 포함합니다. 기존 연구들이 두 개의 이미지를 비교하는 방식에 국한된 접근법을 사용한 것과 달리, 본 연구는 **하나의 이미지 내에서 발생하는 자연스러운 모호성** 문제를 해결하는 데 주력합니다.

LLaVA 모델을 사용하여 **명확화 질문**을 생성하고, 해당 질문에 대해 **인간 또는 GPT-4o**가 답변을 제공함으로써 최종 VQA 성능을 향상시켰습니다. 실험 결과, 제안된 접근 방식은 VQA 정확도를 최대 **11% 향상**시켰음을 확인했습니다.

---

### 🔍 **주요 특징**
- ✅ **명확화 질문 생성**을 통한 모호한 객체 참조 해결
- 🚀 **추가 학습 없이** 성능 향상 달성
- 🧩 **LLaVA-v1.6-7b-hf 모델** 기반 구현
- 📈 **VQA 정확도 최대 11% 향상**
- 💡 **실제 환경에서의 활용성 향상**

---

### 📊 **실험 결과**
#### ✅ **VQA 정확도 향상**
| 조건                  | 정확도(%) |
|----------------------|------------|
| Baseline (명확화 없음)| 61.66      |
| 명확화 질문 + GPT-4o  | 69.33      |
| 명확화 질문 + 인간    | **73.00**  |

#### 🏃 **성능 분석**
- 명확화 질문이 모델의 **객체 참조 능력**을 향상시킴
- **인간 응답**이 GPT-4o 응답보다 더 높은 성능을 달성
- **8~11%의 성능 향상**으로 VQA 작업에서 명확화 질문의 중요성 입증

---

### 🧪 **실험 설정**
- **데이터셋:** GQA 데이터셋 (모호성 유발 질문으로 수정된 무작위 300개 샘플)
- **모델:** llava-v1.6-7b-hf
- **평가 지표:** VQA 정확도, 명확화 질문 생성 효율성
