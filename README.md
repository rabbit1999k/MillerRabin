# Miller Rabin <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/> 

> 2021.04
</br>

## Theory

> 홀수 n이 소수인지 판별 `with. Fermat`
1. n이 소수일 경우, n-1 = 2<sup>s</sup>d &nbsp; <i>(s는 정수, d는 홀수 => n-1 을 계속해서 2로 나눈 형태)</i>
2. `3`,`4` 중 한가지 성립
3. a<sup>d</sup> ≡ 1 (mod n)
4. a<sup>2rd</sup> ≡ -1 (mod n)  

</br>

5. 위와 같은 이론을 바탕으로 `Miller-Rabin 소수판별법`은 `6`,`7`번이 성립하면 `합성수`라는 강한 증거가 된다.
6. a<sup>d</sup> &#8802; 1(mod n)
7. a<sup>2rd</sup> &#8802; -1 (mod n) 

</br>

## Algorithm

1. n-1 = 2<sup>k</sup>q
2. random a &nbsp;&nbsp;<i>(1 < a < n-1)</i>
3. if <b>a<sup>q</sup> mod n = 1</b> then return 아마 소수
4. for j=0 to k-1
5. &nbsp;&nbsp; if <b>a<sup>2jq</sup> mod n = n-1</b> then return 아마 소수
6. return 합성수  

