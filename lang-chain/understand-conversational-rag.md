### reference 
- https://python.langchain.com/v0.2/docs/tutorials/qa_chat_history/

##### PREREQUISITES 
- Chat History : https://python.langchain.com/v0.2/docs/concepts/#chat-history
- Chat models : https://python.langchain.com/v0.2/docs/concepts/#chat-models
  - Language models로써, 메세지들을 인풋으로 받고, 챗 메세지들을 아웃풋으로 내보내는 형태
  - LLM에 비해 비교적 새로운 모델로써, System 메세지, 사용자 메세지, AI 메세지를 구분할수 있게 도와줌
- LLMs (Large Language Models) : https://python.langchain.com/v0.2/docs/concepts/#llms
  - Chat models에 비해 오래된 모델, 문자열을 입력으로 받고 출력으로 보내는 모델
  - 인간의 언어를 이해하고 생성하기 위해서 거대한 양의 데이터가 학습된 AI 모델, (질문과 답, 요약, 번역, 완성 등을 수행한다)
- Embeddings : https://python.langchain.com/v0.2/docs/concepts/#embedding-models
  - Embeddings 모델은 text의 vector 표현을 생성한다. 벡터는 글자의 의미론적 의미를 담고 있는 숫자의 배열이다. 이 방법으로, 가장 비슷한 의미를 가지는 문자를 찾는 수학적 검색에 이용될 수 있다.
- Vector stores : https://python.langchain.com/v0.2/docs/concepts/#vector-stores
  - 비정형화된 데이터를 저장하고 검색하는 일반적인 방법은 이를 임베딩하고 임베딩한 결과를 저장하는 것. 구조화 되지 않은 query를 임베딩 하고, 그 값에 가장 가까운 임베딩된 벡터를 되돌려 받는다.
  - vector stores는 임베디드된 백터를 저장하고, 백터 검색을 수행한다.
  - vector stores은 metadata도 갖고 있어서, 검색전에 filtering 수행이 가능함
- Retrieval-augmented generation : https://python.langchain.com/v0.2/docs/tutorials/rag/
  - LLMs 으로 만들 수 있는 정교한 어플리케이션 중 하나가 Q&A chatbot 인데, 이런 어플리케이션은 RAG(Retrieval Augmented Generation) 라고 알려진 테크니크를 사용한다. 
- Tools : https://python.langchain.com/v0.2/docs/concepts/#tools
  - 툴은 모델에 의해서 호출 될 수 있게 만들어진 utilities 이다.
  - 입력은 모델에 의해 생성되고, 결과 또한 모델로 전달되도록 디자인 되어있다.
  - 모델이 코드 일부를 컨트롤 할 때나, 외부 API 호출을 원할 때 툴이 사용 되어 진다.
  - 툴은 이름, 어떤 일을 하는지, input 포맷(json), 함수 로 구성된 값을 모델에게 전달 해야 하며, 툴이 모델에 바인딩 될 때, 컨텍스트 로써 해당 정보를 전달 한다. 
  - 1) API 호출에 대해 튜닝 받은 모델은 툴을 더 잘 사용한다. 2) 툴의 이름, 어떤일을 하는지, input 스키마가 잘 정의되어 모델에게 넘겨질 수록 모델이 툴을 선택하기 좋다 3) 복작한 스콥의 툴 보다 단순한 스콥의 툴이 모델이 사용하기 더 쉽다. 
- Agents : https://python.langchain.com/v0.2/docs/concepts/#agents
  - LLM을 추론(reasoning) 엔진으로 삼아서 특정 인풋에 무엇을 수행해야 할지 고려하는 시스템이다. 결과가 다시 agent 안으로 들어가서 액션을 더 수행해야 할지 그만해야 할지 결정을 한다.
  - Lang Graph 는 매우 컨트롤이 잘 되고, 커스터마이즈된 agent를 생성하는것에 목표를 둔 확장 시스템이다. 
  - AgentExecutor 는 레거시 시스템이다.
  - ReAct agents : agent를 설계 하는 인기 있는 구조이다. 반복적인 프로세스에서 reasoning 과 acting 을 결합했다.
    -  model인 인풋과 이전에 일어난 일을 기반으로 어떤 응답을 취할지 생각한다.
    -  model은 가능한 툴에서 하나의 액션을 취한다.
    -  model은 tool을 아규먼트를 생성한다.
    -  agent runtime (executor) 은 선택한 tool을 구문 분석하고, 생성한 arguments를 이용해서 호출을 한다.
    -  executor은 model 에게 tool의 결과를 반환한다.
    -  agent가 결과를 선택하기 전까지 이 과정은 반복 된다. 



```
```
