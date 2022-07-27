- 🔥 TIL Rules 🔥

ㅡ[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2F2022_TIL&count_bg=%235B9231&title_bg=%236AD7CA&icon=&icon_color=%23577622&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)


    - TIL은 Today I Learned의 약자로, 개발자들이 매일 공부하거나 코딩한 내용을 정리하여 깃허브에 일일 커밋하는 챌린지다. 일종의 Github Contribution 잔디밭 채우기 챌린지다.
    
    
    -  2022년 TIL은 일자별로가 아닌 카테고리별로 깔끔하게 정리하기로 했다. 2021년에는 사적인 일정 내용도 많아서 Private 상태로 두었는데 2022는 Public으로 해둘 계획. 

Statistics
- [충분통계량(Sufficitent Statistics)](https://hidemasa.tistory.com/196)

- NLP paper
    
    [https://github.com/SOOJEONGKIMM/Paper_log/issues/9](https://github.com/SOOJEONGKIMM/Paper_log/issues/9)
    

- Algorithm(Coding Test)
    - Queue와 Deque: deque가 queue보다 빠르다. queue의 pop()은 O(N)인 반면, deque의 popleft()은 O(1)이다.
    - 정규 표현식 외워두고 사용하면 문자열 문제에서 용이하다.
        - ex) 신규아이디추천(프로그래머스)
            
            [프로그래머스](https://school.programmers.co.kr/learn/courses/30/lessons/72410/solution_groups?language=python3)
            
            ```
            import re
            
            def solution(new_id):
                st = new_id
                st = st.lower()
                st = re.sub('[^a-z0-9\-_.]', '', st)
                st = re.sub('\.+', '.', st)
                st = re.sub('^[.]|[.]$', '', st)
                st = 'a' if len(st) == 0 else st[:15]
                st = re.sub('^[.]|[.]$', '', st)
                st = st if len(st) > 2 else st + "".join([st[-1] for i in range(3-len(st))])
                return st
            ```
