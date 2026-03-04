# Azure AI Search 구성 및 노트북 실습

## Azure AI Search 생성

1. `Microsoft Foundry`에서 생성한 프로젝트의 Microsoft Foundry 리소스를 클릭합니다.
    
    ![image.png](./images/image.png)
    
2. `Resource group`을 기록해 둡니다.
    ![resource group checking](./images/resourcegroup_check.png)

3. 브라우저의 새 탭에서 [`Azure Portal`](https://portal.azure.com/)에 접속합니다.
4. 상단 메뉴 검색창에 `AI 검색`을 입력합니다.
5. `Microsoft Foundry | AI Search` 화면에서 `+ 만들기` 버튼을 클릭합니다.
6. `구독`을 선택하고 기록한 `리소스 그룹`을 선택하고 아래와 같이 구성합니다.
    - 서비스 이름 : `<alias>-ai-search`
    - 위치 : `(Asia Pacific) Korea Central`
    - 가격 책정 계층은 `Standard(표준)` 으로 둡니다.
7. 나머지 설정은 그대로 두고 `검토 + 만들기` 버튼을 클릭하고 `만들기` 버튼을 클릭하여 리소스를 생성합니다.

## Azure AI Search 구성

1. [`Microsoft Foundry 포털`](https://ai.azure.com/)로 이동합니다.
2. 프로젝트 화면 왼쪽 메뉴 하단의 `관리 센터`를 클릭합니다.
3. 왼쪽 메뉴 `리소스`에서 `Connected resources`를 클릭하고 `+ 새 연결` 버튼을 클릭합니다.
4. `Azure AI 검색`를 선택합니다.
5. 리스트에서 생성한 `<alias>-ai-search`의 `연결 추가` 버튼을 클릭합니다.
    
    ![image.png](./images/image%201.png)
    
6. `연결됨` 로 변경되면 `닫기` 버튼을 클릭합니다.

### AI Search 구성 후

1. 왼쪽 메뉴에서 `관리 센터` 메뉴를 클릭합니다.
2. `Connected resources` 메뉴를 클릭합니다.
3. 생성한 `<alias>aisearch` 항목을 클릭합니다.
4. 아래와 같이 `.env 파일`을 업데이트 합니다.
    
    ![image.png](./images/image%202.png)
    
    ```bash
    SEARCH_INDEX_NAME="healthtips-index"
    SEARCH_ENDPOINT=<search-endpoint>
    SEARCH_API_KEY=<search-api-key>
    ```

### 노트북 실행

다음의 노트북을 차례대로 실습 합니다.
* [1-basic-chat-completion.ipynb](./1-basic-chat-completion.ipynb) 
* [2-embeddings.ipynb](./2-embeddings.ipynb)
* [3-basic-rag.ipynb](./3-basic-rag.ipynb)