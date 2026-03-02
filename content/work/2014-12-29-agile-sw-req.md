---
layout: post
title: "Agile Software Requirements - Dean Leffingwell"
---

<img class="alignnone size-full wp-image-58" src="https://raw.githubusercontent.com/midaeng/articles/gh-pages/images/blog/ASR_scaled_agile.png"/>  

팀 단위의 Scrum을 진행하다가, 좀 더 큰 규모로 넓히기 위한 프랙티스를 공부하는 중입니다.  
**공부하면서 조금씩 채워지는 페이지입니다.**

<blockquote> Agile Software Requirements, Lean Requirements Practices for Teams Programs and the Enterprise (Dean Leffingwell) 라는 책을 보고 있어요. </blockquote> 

## 전체 구성
큰 조직이 애자일 프레임웍을 갖추려면 어떤 모양이 이상적인지, 그것을 요구사항의 관점에서 풀어내고 있는 책으로 아래와 같이 파트 4개로 구성되어 있다.  

**Part I Overview: The Big Picture**  
책 전체의 오버뷰로 대규모 조직에서는 어떤 모양새로 팀을 꾸리고, 큰 조직의 모양을 짜야할지에 대한 내용이 담겨있다.  

**Part II Agile Requirements for the Team**  
팀 레벨에서 다루어야 하는 역할, 산출물, activity 등에 대해 기술하고 있다.  
혹시 회사에서 스크럼을 접해봤다면 그것이 바로 팀 레벨에서 수행되는 것의 일부일 것이다. 밖에서 스크럼을 접해봤더라도 아마 팀 레벨이 대부분일 것이고 아주 미미하게 프로그램 레벨이지 않을까 생각됨.  

**Part III Agile Requirements for the Program**  
프로그램 레벨, 즉 제품 레벨에서 필요한 역할, 산출물, activity 에 대해 기술하였다.  
우리는 제품을 만들고 있기 때문에 실질적으로 이 부분에서 수행되는 것들에 대해서 고민하고 다루어야 한다. (개인적인 생각)  

**Part IV Agile Requirements for the Portfolio**  
그래서 대규모 조직이 이미 애자일 조직으로 꾸려져 있고 자리를 잡은 상태라면 '전체적인 포트폴리오를 어떻게 가져갈까'에 대한 부분이다.  
Agile을 잘하고 있고 그래서 enterprise agile을 고민한다는 많은 회사들을 보면 그 규모가 많아봤자 500명 정도가 아닐까 싶다. 게다가 우리회사는 SW뿐만 아니라 HW가 완제품으로 나가는 조직이기 때문에 그 인원을 산정하면 수천단위로 늘어난다. 이런 조직에서의 agile을 전파하고, 수행하며, 경험해본 사람은 많지 않을거라 본다. 하여간, 우리회사는 아직 여기까진 시기상조이므로 회사 안에 있는 사람들은 파트 3까지만 보고 잘 적용해도 엄청 잘한다는 소리 들을 듯.  

----------------------------------------    

### Part I Overview: The Big Picture (CH 1~5)
![Scaled Agile Framework Big Picture](/images/blog/ASR_scaled_agile.png)

#####Chapter 1 A Brief History of Software Requirements Methods


#####Chapter 2 The Big Picture of Agile Requirements
크게 보면 **Team level, Program level, Portfolio level** 세가지로 구분할 수 있다.  
**1. Team level** : agile 팀은 5~9명 정도로 구성하고, iteration과 release에 포함되는 user story를 define, build, test 해야 한다.  
**2. Program level** : ART(Agile Release Train)은 iteration과 milestone에 대한 규칙적인 time box를 가져야 하며, 날짜, quality에 대해서는 반드시 명확한 기준을 가져야 하지만, scope은 변경될 수 있다.  
  - 또 Program level에서는 시스템에 대한 feature 정의에 대한 책임을 가져가기 위해 우리가 알고 있는 Product manager가 있어야 한다.  
**3. Portfolio level** : a mix of investment themes에 대해 다루어야 함. requirements value delivery stream에 대해 포커싱 함.  

**1. Team level**  
Agile team은 implement, test code, building을 모두 수행해야 한다.  
<blockquote> In its daily work, the team is supported by architects, external QA resources, documentation specialists, database specialists, source code management (SCM)/build/infrastructure support personnel, internal IT, and whoever else it takes such that the core team is fully capable of deining, developing, testing, and delivering working and tested software into the system baseline.</blockquote>  
**위의 문장에서 알 수 있는 것**  

* 한 팀 안에서 모든 역할이 수행이 되어야 한다.  
  * 즉, 우리 회사처럼 조직이 세분화되고 심지어 사이트가 다른 상황에서, 담당자가 누군지 찾아내고 한 자리에 회의를 소집해서 그 사람들과 커뮤니케이션을 시도하기까지 드는 시간과 노동력은 정말 엄청난 낭비라는 의미.  
  * 뭔가를 만들어야하는데 남의 팀 사람에게 너가 이거 해야한다고 말할 때 싸움이 발생한다.  
  * 우리팀이 아니고 남의 팀 사람이 해야한다는 생각이 드는 순간 내가 만들고 있는 이게 뭐든 내 것이 아니게 된다. 하물며 같은 팀 내에서도 쟤보다 내가 일을 더 많이하면 짜증날텐데, 다른팀이면 오죽하겠는가.  
  * (20141229 추가) 사이트가 떨어져있는 것이 문제는 아니라는 생각이 듦. 실리콘밸리의 유수 회사들을 보면 여러 국가에 걸쳐 사이트가 분리되어 있지만 협업이 잘 이루어지는 곳이 많다. 과연 사이트가 떨어져있는 것이 문제일까? 떨어져있다는 생각이 안들도록 마치 옆에서 일하고 있는 것처럼 환경을 꾸며주는게 중요하다.  
  => Facebook, TW사례 : 벽 한쪽에 빔 프로젝터를 이용하여 다른 사이트의 모습을 보여주고 있다. 만약 일을 하던 중에 의문이 드는 것이 있어서 NY에 있는 Matthew와 이야기를 해야한다면, 그 벽 앞에 가서 Matthew를 불러달라고 해서 이야기할 수 있다. (물론 상대방이 뭔가에 집중하고 있었을 때 이렇게 자꾸 불러댄다면 인터럽트의 성격이 짙겠지만, 사이트가 다른 것이 전혀 문제될 것이 없다는 이야기를 하고 있는것임)   
* 흔히 enterprise 조직에서는 component 팀과 feature 팀이 혼재하고 있다.  
보통 **component 팀**은 shared infrastructure, subsystems, and persistent, service-oriented architectural components에 집중하고, **feature 팀**은 vertical, user-facing, value-delivery initiatives에 집중한다. 하지만 궁극적으로는 program backlog에 기반하여 work 단위로 업무를 하려면 팀은 self organizing, recognize할 수 있어야 한다.  
  * Product owner의 역할이 상당히 중요함. 이건 뒤에 나오니깐 뒷부분에 자세히.  
  * Developers and Tester : 저자는 개발자 2명에 Tester 1명 정도 비율로 적용했다고 함.  
  * user story 양식 : **As a (user role), I can (activity), So that (Business value)**  
  => 팀은 user's role과 business benefit 두가지 모두에 집중하는 것을 배워 새로운 functionality를 제공해야 함.   
    

**2. Program level**  

* Responsibilities of the Agile Product Manager in the Enterprise  
  * Own the Vision and program (release) backlog  
  * Manage release content  
  * Maintain the product Roadmap  
  * Build an effective product manager/product owner team  
* Releases and Potentially Shippable Increments : 여러 feature와 arch가 작업한 것을 integration 하는 단계. 여러 팀에서 작업한 것을 합치는 과정이므로 **추가 작업을 위한 빈 백로그를 준비해두는 것도 요령임.** (Agile 2013 conference에서 Lego TDD 세션 중 맨 마지막 과정이었던 8명 한팀이 모두 모여 놀이동산 만들기 할 때, 각자가 만든 것을 하나로 합치는 과정에서 높이나 크기를 맞추기 위해 시간이 필요했던 것처럼.)  
* Product Management : enterprise에서는 겹치는 역할이 있는데, product manager와 product owner 임. 소규모 scrum 팀에서는 product owner 정도면 커버가 가능하지만 대규모로 가면 전체를 보기에는 부족하다. 하여 enterprise를 위한 product manager 역할이 필요하다.  


**3. Portfolio level**  

* Investment Themes : the result of the decision process is a set of themes. Themes have a much longer life span than epics, and a set of themes may be largely unchanged for up to a year or more.  


#####Chapter 3 Agile Requirements for the Team#####

#####Chapter 4 Agile Requirements for the Program#####

#####Chapter 5 Agile Requirements for the Portfolio#####
  



### Part II Agile Requirements for the Team (CH 6~12)
* 파트 2에서는 팀 레벨에서 수행할 수 있는 애자일 요구사항에 대해 이야기하고 있다.  
* 총 7개의 장으로 구성되어 있으며, 각각의 제목을 보면 우리가 그동안 자주 들어왔던 것임을 알 수 있다. 특히 스크럼에 대해 들어보거나 수행했던 사람들이라면 그리 낯설지 않을 것이라 생각됨.  
* 팀 레벨에서 가질 수 있는 역할과 수행해야하는 activity 등에 대해 기술하고 있음  

#####Chapter 6 User Stories#####

#####Chapter 7 Stakeholders, User Personas, and User Experiences#####

#####Chapter 8 Agile Estimating and Velocity#####

#####Chapter 9 Iterating, Backlog, Throughput, and Kanban#####

#####Chapter 10 Acceptance Testing#####

#####Chapter 11 Role of the Product Owner#####

#####Chapter 12 Requirements Discovery Toolkit#####



### Part III Agile Requirements for the Program  (CH 13~19)
* 각 장의 제목을 보면 알 수 있듯이 사업부 차원에서 바로 적용할 수 있는 부분이 바로 program level이다. 팀 레벨에서 만들어낸 요소들을 하나로 묶어내야 한다. 
* 제품의 비전, 제품을 이루는 feature와 로드맵이 왜 필요한지, 제품 책임자인 product manager가 팀 레벨의 product owner와 어떤 차이가 있는지 설명하고 있다.
* 15장의 내용에 그림이 몇개 나오는데, 바로 release에 대한 내용이다. 우리 회사는 제품을 만드는 회사라서 일반적인 SW 회사에서 릴리즈하는 방식과 동일하게 적용하는건 불가하다. 즉, 기능 단위의 SW를 프레임웍과 integration을 해야하고, 이를 또 사업자에 따라 제품 레벨로 SW를 한번 통합하는 과정을 거쳐야하는데 15장과 16장에서 그에 대한 아이디어를 얻을 수 있겠다. 

#####Chapter 13 Vision, Features, and Roadmap#####
![Ch 13](/images/blog/ASR_ch13.png)  

#####Chapter 14 Role of the Product Manager#####
![Ch 14](/images/blog/ASR_ch14.png)  

#####Chapter 15 The Agile Release Train#####
![Ch 15](/images/blog/ASR_ch15.png)  

#####Chapter 16 Release Planning#####

#####Chapter 17 Nonfunctional Requirements#####

#####Chapter 18 Requirements Analysis Toolkit#####

#####Chapter 19 Use Cases#####




###Part IV Agile Requirements for the Portfolio (CH 20~24)###
사실 여기는 우리 회사에서는 시기상조인 부분인 것 같다. 미리 준비하는 것도 좋지만 아직 기초도 안되어 있는 상태에서 상위 레벨을 고민하는게 어떤 의미가 있을까? 지금은 Part 3에 좀 더 집중해보자.  
 
#####Chapter 20 Agile Architecture#####

#####Chapter 21 Rearchitecting with Flow#####

#####Chapter 22 Moving to Agile Portfolio Management#####

#####Chapter 23 Investment Themes, Epics, and Portfolio Planning#####







