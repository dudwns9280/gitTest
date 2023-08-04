# gitTest  
## 목적  
git revert에 대해서 공부하는 repository  
여러 기능을 개발 후 각각 다 merge를 통해 develop 브런치에 반영했으나  
그 기능 중 특정한 기능을 제외한 나머지를 배포하고싶을 시 revert를 통해서 그 상황을 구현해보려고 함.  

## 환경
feat/1  
feat/2  
feat/3  
feat/4  
각각의 브런치를 만들어서 develop 브런치에 merge함.  
그 중 feat/2번의 반영 사항을 되돌리고 싶음.  

## 방법

1) git log를 통해 우선 feat/2의 commit id를 알아냄.  
2) git revert -m 1 fdd6f9ea754da343622567cf2fc5d967a943ddc6
3) 충돌난 코드에 대해서 충돌 반영 후 git revert --continue를 통해 revert 진행.
4) 해당 내용 revert 완료 후 git push를 통해 develop 브런치에 push
