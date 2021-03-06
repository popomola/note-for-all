# 데이터프레임
기본개념 
! 데이터프레임을 볼 때는 컬럼->인덱스->밸류 순서로 본다.
! 데이터프레임은 2차원이다(구성요소는 컬럼, 인덱스, 밸류) 시리즈는 1차원이다(구성요소는 2개다. 인덱스, 밸류)
! 시리즈와 마찬가지로 데이터프레임도 순서가 있다. 행방향으로 순서가 있다. 즉, 행 하나하나씩이 단위다.
! 데이터프레임에서 컬럼 하나를 가지고 나오면 시리즈로 나온다.


기본 사용법
! 1 데이터 파일을 불러온다.
! 2 컬럼을 확인해서 원하는 컬럼을 골른다.
! 2-1 (때에 따라 컬럼의 이름을 내 마음대로 바꾼다.)
! 3 인덱스를 확인한다.
! 4 밸류에 결측치가 없는지 확인한다.
! 4-1 결측치는 지우거나 채워준다. 보통은 지우지는 않는다.
! 5 원하는 값들이 선별되었다면 내가 쓸 데이터프레임이 만들어진다.
!  위와 같은 정제과정을 거치면 데이터프레임을 만들 수 있다.

# API
기본개념 
! api를 사용하기 위해서는 url + 인증키 + 옵션이 필요하다.(이용하고 싶으면 이 3개 확인필요)
! 내 컴퓨터가 무언가 요청하면 어딘가에 있는 서버가 응답을 보내준다.
! 크롤링에서 이 응답의 내용은 코드가 된다.
! api로 데이터를 요청할 때는 응답의 내용이 데이터가 된다.
! 코드가 전송될 때는 html+Css+javascript 코드가 전송되어 온다.
! 데이터가 잔송될 때는 json 혹은 xml 형태로 데이터가 전송된다.
! json은 리스트 안에 딕셔너리가 들어 있는 형태다. 딕셔너리 안에 데이터가 키와 밸류로 저장되어 있다.

# 기술노트
! pandas에서 데이터프레임과 시리즈, 시리즈와 시리즈를 합치고 싶다면 pd.concat를 사용할 것. 기본은 같은 column을 갖는 row들을 위아래로 붙이는 것. aixs=1로 주면 서로 다른 column을 가진 애들까리 합칠 수 있다.
! pandas에서 loc과 iloc 이 두 개가 대표적인 데이터프레임의 값을 가져오는 방법. 
! iloc이 제일 편해 보인다. iloc(행인덱스, 열인덱스) 헷갈리면 검색 ㄱ
! numpy에서 랜덤한 숫자를 생성하고 싶다면 numpy.random.randint(시작, 끝, 사이즈)을 지정하면 된다. 사이즈의 크기에 맞는 array를 return한다. 자세한 건 검색 ㄱ
! 


# 데이터 시각화
! matplotlib는 기본 영문 폰트를 쓴다. 때문에 한글 인식이 안 된다. 이를 해결하기 위해
plt.rc('font', family='Malgun Gothic') 이 코드를 plt.show() 전에 붙여쓰자.
! matplotlib.pyplot.hist는 데이터의 수가 작을 때는 뭔가 왜곡?이 일어난다. 때문에 np.histogram을 이용하는 편이 낫다.
! matplotlib.pyplot.plot은 선 또는 마커를 그리기 위한 기초적인 함수다. plot에 대한 자세한 것은 검색 ㄱ. 매개변수로 받을 수 있는 형태가 굉장히 다양하다.
! matplotlib.pyplot 모듈의 xlabel, ylabel 함수를 사용하면 그래프의 x, y 축에 대한 레이블을 표시할 수 있다. loc은 위치지정. fontdict 매개변수도 있다. 검색 ㄱ 혹은 파이썬 노트 참고
! matplotlib.pyplot.legend는 범례를 표현한다. 검색 ㄱ 혹은 파이썬 노트 참고
! matplotlib.pyplot 모듈에는 xlim, ylim을 통해 보여지는 축의 범위를 지정할 수 있다. 혹은 axis를 써도 된다.
! matplotlib에서 선 종류는 plot함수 안에서 매개변수를 통해 지정한다. 이 종류 지정하는 것도 방법이 여러 가진데... 굳이 그럴 필요가 있나 싶은 것도 있다. 자동화를 위해서 있는 건가?
! matplotlib에서 선의 끝?도 plot에서 매개변수로 지정할 수 있다... plot의 매개변수가 꽤나 많다.
! matplotlib에서 마커도 plot으로 한다... 아주 무시무시한 plot이다. 일례로 'bo'는 blue circle을 그래프 상에서 표시한다. 'bo-'는 마커 사이의 공간을 선으로 연결시킨다.
! matplotlib에서 색상 지정도 plot으로.
! matplotlib에서 plot(color, marker, linestyle)으로 하면 색상, 마커, 선 스타일 삼위일체로 할 수 있다. 대박
! matplotlib에서 fill_between을 쓰면 그래프의 아래의 영역을 채워준다.
! matplotlib에서 그래프 상에 수평선을 그리려면 axhline 혹은 hlines 수직선을 그리려면 xvline 또는 vlines 사용 매개변수는 검색 ㄱ 혹은 파이썬 노트 참고
! 

# 머신러닝
! 어쩌다 등장했나. IBM의 한 직원이 컴퓨터가 체커를 플레이 할 수 있도록 하는 프로그램을 만들면서 시작되었다고 한다. 머신러닝의 첫 시작은 특정의 국소 기능을 수행하라고 지정하는 게 아니라 그 국소 기능을 수행할 수 있도록 학습할 것을 지정하는 것이다. 예를 들어 체커를 플레이하는 전략을 심어주는 게 아니라 체커 하는 법을 가르쳐서 스스로 전략을 짤 수 있게 하는 것. 컴퓨터는 기본적으로 프로그래머의 명령만을 따르는데, 명령으로서 배우라고 지시하는 것이다.
! data set이 있을 때 하나의 row를 example이라 부르고, column을 feature라고 한다.
! 예측하고자하는 값을 target이라고 한다. 
! 데이터 수집 > 데이터 정제(데이터 축출, 시각화 등) > 모델 선택 > 모델 평가
! 머신러닝에서 자꾸 벡터 잇찌랄을 했던 게... 시각화를 위한 개념적인 말이었던 것 같다... 혹은 기하학적인 뭔가를 표현한다든지...
! 
