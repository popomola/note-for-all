# 노트

# 0일차
! React의 폴더를 만들고 싶다면 npx create-react-app 폴더이름 이래야 한다.

# 1일차
! 리액트는 컴포넌트 별로 기능을 잘개 잘 쪼개는 게 중요한듯..?
! 그러니까, 하나의 컴포넌트는 하나의 기능만 수행하도록. 버튼이면 버튼기능만 수행하게.
! 컴포넌트의 parameter값으로 리스트도 넣을 수 있다.
! 문제는 리스트를 인자값으로 받은 컴포넌트가 리스트 안에 들어 있는 딕셔너리에 어떻게 접근하냐는 것이다.
!예를 들어서, 
const userDB2 = [
    {
        writer:"21학번/경제",
        date:'2021-8-19',
        title:'주식이...',
        body:'다 꼴았어요,,',
    },
    {
        writer:"19학번/전장공학",
        date:'2021-8-19',
        title:'비트가...',
        body:'나무아미타불,,',
    },
    
]
이렇게 리스트가 있고, 이 리스트를 PostList 컴포넌트가 받고, 그 안에 있는 PostItem 컴포넌트가 props으로서 받은 리스트에 접근한다고 했을 때, 단순히 userDB[0]이런 식으로만 접근이 가능한가?

! React-Router를 통해 url변경 시 원하는 컴포넌트만 화면에 나타날 수 있도록 하는 기능도 있다.
! Switch는 원하는 것만 화면에 띄워주는데, '/'얘가 path인 경우에는 exact를 path앞에 써준다.
! Router의 Switch를 쓰면 url에 좀 민감해진다. url에 해당하지 않는 컴포넌트는 화면에 안 나옴
! Router가 굉장히 편한 것 같다. a태그를 쓰지 않더라도 Link나 Route를 통해 원하는 페이지를 띄울 수 있으니까. 이때 Link는 a태그와 같은 기능을, Route는 url만 조작.
! Css에서 overflow를 사용하면 박스 안의 콘텐츠를 어떻게 할 수 있다.
! Css에서 box-sizing: border-box를 사용하면 콘텐츠를 담을 수 있는 박스를 만들 수 있다.
! 데이터 표시 방법에 대해서 많이 좀 헷갈린다...

# 2일차
! 컴포넌트 간 데이터 전송 방식에 대해 헷갈린다. 구글링 해도 별로 없다.
! 컴포넌트를 어떤식으로 구성해야 하는지, 어떻게 쪼개야 하는지 좀 헷갈린다.
! React에서는 Modal 컴포넌트를 사용하는 게 쉽다. 그냥 npm install --save react-modal하고, Modal 컴포넌트를 사용하고 싶은 파일에서 import Modal from 'react-modal'하고, isOpen에 bool값을 주면서 열었다 닫았다 하면 된다.
! React에서 JSX안에서 조건문을 쓰고 싶다면, ternary operator말고는 답이 없는 거 같다. 조건에 맞춰 원하는 컴포넌트들을 리턴할 수 있다. 단, ternary operator를 쓰려면 javascript이기 때문에 
return(
    <>
        {a? b : c}
    </>
) 
이렇게 안에다가 해야 한다.

! Route는 폴더가 다른 경우 해당 url로 연결되지 않는 경우가 있다. 그러니까, Components폴더 안에서 특정 파일 내에서 Route를 사용할 때, Component밖에 있는 App함수에서도 Route를 사용해서 Components폴더 안의 특정 컴포넌트를 불러온다면, 화면에 뭔가 나타나지 않는 버그가 발생한다. url이 뭔가 중복되어서 그런 문제가 발생하는 것 같다.
! 컴포넌트에 데이터가 들어가야하는 경우, 해당 컴포넌트를 사용할 환경(맥락), 그러니까 예를 들어
Post파일에서 WritePost컴포넌트를 쓴다고 했을 때, WritePost의 데이터는 props의 형태를 통해 Post파일에서 얻는 게 낫다. 즉, 컴포넌트 파일 자체에서 데이터를 얻기 보다도, 컴포넌트가 쓰이는 맥락에서 데이터를 얻는 것이 독립적이고 기능적인 컴포넌트를 만들기 위해 더 좋은 것 같다.
! React에서는 기본적으로 막 코드를 쓰기보다도 미리 화면의 구성과 데이터 간의 관계를 구상해놓고 코드를 쓰는 게 더 효율적인 것 같다.

# 3일차
! 웹 개발 하는데 참으로 알아야 할 게 많은 듯 싶다. 말 그대로 어떻게 보면 프로그래밍계의 종합 예술 같다. 첨음에는 html, css, javascript만 할 줄 알면 그냥 끝인 줄 알았더만 더 편하게 웹을 개발하기 위한 다양한 라이브러리나 api들이 계속 튀어나오고 쓸 줄도 알아야 한다. 물론 html, css, javascript가 핵심이기는 하지만... 왜냐면 기본적으로 웹개발을 위한 api, 라이브러리들은 javascript기반이니까... 그런데 참 뭔가 많다.
! React에서 import를 할 때 default로 export된 컴포넌트는 {}를 쓰지 않아도 된다. 당연히 export default되지 않은 컴포넌트는 {}로 감싸서 데려와야 한다.

# 4일차
! Redux라는 게 있다. global state를 관리하는 데 도움을 준단다. state의 관리를 더 용이하게 해주고, 관리되는 state와 연관된 로직들을 관리하는 데도 도움을 준단다.
! Redux의 사용은 개발자에게 일정 제한으로 작용할 수 있기 때문에 필요한 경우에만 사용해야 한다. 필요한 경우라면,
앱 전반에 사용되는 state가 굉장히 많을 때, state가 굉장히 자주 바뀔 때, 자주 바뀌는 state의 logic이 복잡할 때, 여러 사람들과 함께 작업을 해야 할 때
! one-way data flow는 하나의 컴포넌트 안에서 하나의 state만 사용될 때의 경우를 말한다. 하지만 하나의 state가 여러 컴포넌트에서 사용되어야 한다면, 문제가 발생한다. state 로직이 복잡해진다.
! Redux는 하나의 중앙화 공간을 제공하여 globally 쓰이는 state를 저장하고, 해당 state에 global이 접근할 수 있도록 한다.
! Redux에서 action은 type field를 갖는 object이다. application에서 발생한 무언가를 설명하는 역할을 한다.
! 이때 action의 type은 action이 하는 역할을 설명할 수 있는 문자 이름이 되어야 한다. 형태를 "속한 영역/이벤트 이름"으로 이름을 짓는다. 또한 payload라는 field에 구체적으로 action이 어떤 일을 하는지 기록한다.
! Redux에서 reducer는 현재의 state와 action를 매개변수로 받는 함수다. 그리고 action의 type에 따라서 어떻게 state를 업데이트 할 것인지 결정한다. 필요하다면 새로운 state를 return한다. if문이나 switch를 통해 원하는 state값을 return 할 수 있다.
! Redux에서 Store는 state를 저장하고 있는 object다.
! Redux에서 Dispatch는 store에 저장되어 있는 state를 변경할 수 있는 유일한 방법이다. action을 pass in 하여 state를 변경한다. action을 dispatch한다는 것은 triggering an event와 같은 의미다.
! React에서 Lifting state up한다는 것은 컴포넌트들이 사용되는 공통된 상위 컴포넌트(ancestor)에서 state를 조절하는 것을 말한다. 즉, 상위 컴포넌트로 state를 lift up한다는 것.

# 5일차
! https://redux.js.org/tutorials/fundamentals/part-3-state-actions-reducers 이 링크로 가면 redux와 react가 준비된 template을 받아 사용할 수 있다. 만약 reducer헷갈리면 방문해서 읽어라.
! Redux와 React에서 중요한 것은 UI가 state에 기반해야 한다는 것이다.
! Redux에서 reducer는 불가침원칙이 3개 있는데 그 중 하나는 이미 존재하는 state의 원본을 바꿀 수 없고, 해당 state를 복사하여 값을 업데이트 해야 한다는 점이다.
! Redux의 reducer 함수가 직접 값이 변화하는 state를 다루지 않고 복사하는 이유는, 함수에서 함수 외부의 변수(값) 혹은 매개변수를 조정하거나 건들이면 application이 꼬일 수 있기 때문이다.
! 즉, 되도록이면 하나의 함수는 외부의 변수 혹은 입력받는 매개변수를 변화시키지 말아야 한다.
! 때문에 따로 state의 복사본을 만들 수 있는 방법을 알고 있어야 한다... 나는 아직 모르겠다.
! 한편 state가 nested되어 있는 경우에는 모든 level마다 값들을 다 바꿔야 한다.
! Redux에서는 reducer를 저장하기 위해 해당 reducer가 수행하는 기능(feature)별로 폴더와 파일을 쪼개서 저장한다. feature상위 폴더에 각각의 기능을 갖는 reducer하위폴더들을 만드는 것.
! 이때 각각의 하위폴더들의 이름은 action의 tpye을 나타내고, 하위폴더 내의 파일들은 action의 내용을 설명할 수 있는 제목으로 만든다. 또한 slice라는 이름을 붙여 기능이 간소화된 reducer임을 표현한다.
! 한편 Redux store는 하나의 root reducer만 필요하다. 때문에 파일들을 다 쪼개면, 하나의 reducer파일에다가 각각의 slice(기능이 최소단위로 쪼개진 reducer파일)들을 임포트 해서 reducer의 형태로 return한다. 자세한 건 검색해라. 헷갈리면. 검색어는 combine reducer로. 
! 어쩄든 쪼갠(slice된 reducer들) 애들을 하나의 파일에다가 불러오면 각각의 reducerslice들은 각각이 맡은 global state를 관장한다. 
! 기본적으로 React관련 된 애들은 기능 별로 작은 단위로 쪼개는 것을 좋아하는 것 같다. 때문에 처음 앱을 디자인 할 때 기능 별로 쪼갤 수 있는 건 쪼개서 분류를 하고 기능을 구별하는 게 중요한듯.
! 그런데 이 귀찮은 것들을 쉽게 만들어주는 녀석이 있다. terminal에서 npm install redux를 하고, root reducer 파일에서 combineReducers를 import하면 된다. 자세한 건 검색 ㄱ

# 6일차
! npm은 pakage manager다. 그래서 뭔 패키지만 깔려 하면 terminal에다가 npm install 잇찌랄 하는 거였다.
! material-ui는 npm이 가지고 있는 여러 패키지들 중 하나다. 필요한 UI들을 가져다 쓸 수 있는 api다. 기본적인 다운로드는 terminal에다가 npm install @material-ui/core 하면 된다. 잘 모르겠으면 공식 사이트에서 검색해도 된다.
! component api에 어떻게 불러오는지, component에 어떻게 쓰는지 나와있다.
! React에서 차라리 material-ui의 Button 컴포넌트를 사용해서 text button형식으로 마치 게시판의 글을 클릭하면 들어갈 수 있도록 하는 형식의 구현을 할 수 있다. 따로 뭐 text그 자체에다가 a태그를 걸어서 링크를 주는 것보다 차라리 text button을 이용해 해당 text를 클릭했을 때, modal이 열리도록 하는 것도 꽤나 깔끔한 방법 같다... 아마도?
!  
