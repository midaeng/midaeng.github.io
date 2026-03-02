---
layout: post
title: "Paper Prototyping : 상기-UX-개발자가 서로 원활한 커뮤니케이션을 하며 요구사항 도출하기"
---

개발을 하다보면 나중에 가서 communication 문제로 인해서 서로 다른 것을 생각하고 있다는 것이 밝혀집니다.  

그래서 수행했던 것이 페이퍼프로토타이핑(Paper Prototyping)인데요,  

> 개발 초기에, 
> 코드 한줄 없이 아이디어나 컨셉 수준에서도, 
> 누구나, 
> 종이를 가지고, 
> 마치 실제 구현된 시스템인 것 처럼, 
> 동작을 시켜보는 activity 입니다. 

* 내 머릿속에 있는 아이디어를 추상적으로 말로만(viral) 전달하는 것이 아니라, 시각적(visual)으로 표현함으로써 함께 일하는 사람들과 의견을 나누어 서로의 눈높이를 맞추고, 
* 그동안 미처 끄집어내지는 못했지만 존재하고 있었던 문제점들, 혹은 잠재되어 있던 risk 들을 미리 끄집어낼 수 있고,
* 사용성 측면에서 이게 정말 사용자가 주로 사용하는 시나리오 인지 다시 한번 생각해볼 수 있습니다.  

실제로 제품을 개발하며 흔히 볼 수 있는 상황인,  
**초반에 요구사항이 분명하지 않거나, 아이디어 단계에서 잘못된 기획으로 인해 그대로 개발하게 되고 그것이 시제품 단계까지 간다면??**  
시간이 지날수록 그것을 고치는 비용이 점점 더 커지게 되겠죠. 결국엔 마지막에 가서 뺄지 말지 의사결정을 해야 하겠구요.  

communication에 의한 문제, 사용 중 발생할 수 있는 Performance 관련 risk 등에 대해서 코드를 개발하기 이전에 미리 도출해볼 수 있습니다.  

Paper prototyping 소개 자료는 slide share에 공유해두었어요.  
소규모로 워크숍을 할 수 있도록 자세한 진행 방법도 적어두었습니다.  

<iframe src="//www.slideshare.net/slideshow/embed_code/43301942" width="476" height="400" frameborder="0" marginwidth="0" marginheight="0" scrolling="no"></iframe>

#### 사례
사례로 webOS TV에 들어가는 Camera 앱에서 Paper Prototyping을 진행해보았습니다. (2nd version / 2014.06.05 수행)  

1. Camera 앱 Setting 관련하여 시나리오에 두 장에 걸쳐 기술된 resolution setting 기능 
- resolution에 대해서는 사실 1장이 전부였음.  


2. Camera에 진입하는 부분까지 포함하여 시나리오 두장에서 뽑아낸 story line - 6단계   

<img class="alignnone size-full wp-image-58" src="https://raw.githubusercontent.com/midaeng/articles/gh-pages/images/blog/pp-2.png"/>   


3. 이걸 바탕으로 사용자 시나리오를 장면이 바뀌는 것에 따라 그려봅니다.  

<img class="alignnone size-full wp-image-58" src="https://raw.githubusercontent.com/midaeng/articles/gh-pages/images/blog/pp-3.png"/>   
  
    **유의 사항 : 메인 시나리오 잡기 (예외 처리는 일단 고려하지 않는다)**  
    - 우선순위가 가장 높은 것을 선택한다는 의미로, 가장 중요한 것 이외의 것들은 예외처리로 간주한다. (즉, 예외처리는 나중에 개발하는 것이고, 시간이 없으면 버릴 수도 있다는 의미)  
    - 기존에는 메인 시나리오와 아닌 것들이 동등한 수준으로 나열되어 우선순위가 잘 안보인다. (중요한 것과 덜 중요한 것에 대한 우선순위화 가능)  
    - 메인이 아닌 시나리오에 대해서도 화면 별로 추가하여 우선순위를 부여할 수 있다.   
    - 또, 어떤 이유에 의해 브랜치 시나리오를 빼야하는 경우 그에 대한 근거가 되기도 함.     
    - 메인 시나리오가 가운데 있고 예외 케이스를 추가하는 형태로 나열하면 Test Case 뽑기가 쉬워진다.   
    - 기존에 시나리오를 작성하던 것처럼 Flow chart로 작성하면 눈에 잘 안들어오고 헷갈림 (브랜치가 많아지면 더더더!!!)  
    - 사용성 측면에서 정말 저렇게 쓰는지 다시 한번 검토해볼 수 있음   

  
**4. 2번에서 6개의 화면으로 구성될 것이라고 예상했던 것이 실제로 그려보니 총 9 단계가 나왔다.**   
1) 처음엔 7장에 걸쳐 그렸으나, 시뮬레이션을 해보면서 4-1과 5-1이 추가되었음.  
<img class="alignnone size-full wp-image-58" src="https://raw.githubusercontent.com/midaeng/articles/gh-pages/images/blog/pp-4.png"/>   

2) 3과 7에서 모호한 부분이 보였다.   
3) 장면이 넘어가는 것에 대한 정의가 나와 다른 사람이 달랐다. 난 클릭을 한 이후를 그렸고, 다른 사람은 클릭을 하기 바로 이전을 그림으로 나타내고 있었다. 그림을 그려서 각 장면이 의미하는 바를 이야기로 계속 하기 때문에 좀 더 명확한 커뮤니케이션이 되었다.   

<img class="alignnone size-full wp-image-58" src="https://raw.githubusercontent.com/midaeng/articles/gh-pages/images/blog/pp-4-1.png"/>   

**결론 : 사용성 측면에서 정말 사용자가 이런 시나리오로 사용하는지에 대해 논의해볼 수 있음.**  
<img class="alignnone size-full wp-image-58" src="https://raw.githubusercontent.com/midaeng/articles/gh-pages/images/blog/pp-5.png"/>   

실제로 수행해보면서 느낀 장점 및 기대효과는 다음과 같다.  

**1) 우선순위 측면 (내가 만드는게 정말로 End user에게 가치 있는 것인가?**  
- 메인 시나리오를 잡는다는 의미는 우선순위가 가장 높은 것을 선택한다는 뜻이다.  
- 가장 중요한 것 이외의 것들은 예외처리로 간주한다. (즉, 예외처리는 나중에 개발하는 것이고, 시간이 없으면 버릴 수도 있다는 의미)  
- 기존에는 메인 시나리오와 아닌 것들이 동등한 수준으로 나열되어 우선순위가 잘 안보인다.  
- 메인이 아닌 시나리오에 대해서는 뒤에 장면 별로 추가하는 것이 용이하며, 우선순위를 부여할 수 있다.  
- 또, 어떤 이유에 의해 브랜치 시나리오를 빼야하는 경우가 생기면 그에 대한 근거가 되기도 함. (나무의 기둥과 가지라고 생각하면 쉬움)  

**2) Test 측면**  
- 메인 시나리오가 가운데 있고 예외 케이스를 추가하는 형태로 나열하면 Test Case 뽑기가 쉬워진다.  
- 기존에 시나리오를 작성하던 것처럼 Flow chart로 작성하면 눈에 잘 안들어오고 헷갈림 (브랜치가 많아지면 더 헷갈려!!!)  
- 사용성 측면에서 정말 저렇게 쓰는지 UX 뿐만 아니라 개발 및 유관부서가 모두 모여서 다시 한번 검토해볼 수 있다는 것이 가장 큰 장점!!   


Paper Prototyping을 수행한 이후에 나오는 결과물은,  

* QE에서 Test Case를 바로 뽑을 수 있는 정도로 상세화 되고, 그 자리에서 바로 Test Case 도출이 가능하다. (자리에 돌아가서 다시 작성을 해야하는 번거로움을 줄여줌)  
* 요구사항 문서 + 메뉴트리 + UX 시나리오가 하나의 문서로 만들어짐 (PP 과정을 통해 버전 1.0이 바로 나올 수 있다.)  
* documentation에 있어 메인 시나리오를 기준으로 브랜치를 추가하는 방법을 사용하면,  
   1) 기능을 추가할 때 문서 상에 바로 추가하는 것이 가능  
   2) 어떤 위치에 추가해야 할 지 눈에 바로 보임   

 

아, 한가지 중요한게 남았는데.  

> Paper Prototyping을 수행하고 나서 나온 내용들은 반드시 문서화 해야 한다.  
> activity가 끝나고 각자 할 일을 적어가는 것이 아니라 참석자 간 공유할 수 있는 문서로 만들고, 그 문서는 이후에도 지속적인 communication을 할 수 있는 seed가 된다.  

모두 같은 것을 바라보기..   


