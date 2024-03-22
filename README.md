# KDT - 5 NumpyProject

## 기후변화로 인한 기후이상
  

  
#### 역할분담

역할|참여인원
:---:|:---:
자료조사 / 주제 선정 | 박희진, 이승민, 권혁원,고우석
4계절 예측 | 박희진
황사 | 이승민
태풍 | 권혁원
폭설 | 고우석
발표 자료 제작 | 박희진, 이승민, 권혁원, 고우석

<details>
  <summary>
    박희진(4계절 예측)
  </summary>  
    

    
**계절의 길이가 바뀌고 있을까?그렇다면 계절의 시작일을 예상할 수 있을까?**  

### (1) 데이터 확인 및 생성

- 2003년 - 2023년 20년간 대구 날씨 데이터 수집
    - 날짜, 평균기온, 최저기온, 최고기온
- 각 계절의 시작일 데이터 생성
    
    ![계절구분](https://github.com/KDT5NUMPY/KDT-5_NumpyProject/assets/155441547/b7282c50-041b-4f9b-a90e-3e58963027d7)

    
    - 기상청이 제시한 온도로 알아보는 계절 시작일 활용
    - 대구의 평균기온 데이터를 활용하여 시작일 데이터를 생성함.
    - ex) 봄 시작일 : 일평균 기온이 5도 이상 올라간 후 다시 떨어지지 않는 첫날
    
    → 5도 이하를 찍은 날짜 그 다음날을 봄 시작일로 지정
    
    - datetime 객체를 문자열로 반환 후 원하는 형식으로 변환
    - 각 계절마다 기준 월을 두고 며칠 후에 계절이 시작되었는지 계산한 컬럼 추가
        - np.poly1d를 사용하여 해당 데이터에 대한 수식을 생성하고 이를 바탕으로 미래의 계절 시작일을 예측
- 각 계절 길이 데이터 생성
    - 생성한 각 계절 시작일을 이용하여 계절의 길이 데이터 생성
        - np.poly1d를 사용하여 해당 데이터에 대한 수식을 생성하고 이를 바탕으로 미래 계절 길이 예측
    

### (2) 그래프 결과

![four_season](https://github.com/KDT5NUMPY/KDT-5_NumpyProject/assets/155441547/9c1f4882-41d0-40a6-b9d9-388d0f4b74c7)

<div align="center">
  <img src="https://github.com/KDT5NUMPY/KDT-5_NumpyProject/assets/155441547/9c1f4882-41d0-40a6-b9d9-388d0f4b74c7" alt="Image">
</div>


<div align="center">
  [봄 시작일 예측]

  2030년 : 3월 4일

  2035년 : 3월 2일

  2040년 : 3월 1일
</div>


![summer_date](https://github.com/KDT5NUMPY/KDT-5_NumpyProject/assets/155441547/d02943f5-767b-4000-be69-7c4c893101f6)

<div align="center">
 [여름 시작일 예측]

  2030년 : 6월 6일

  2035년 : 6월 3일

  2040년 : 6월 1일
</div>


![fall_date](https://github.com/KDT5NUMPY/KDT-5_NumpyProject/assets/155441547/aea9b46b-1819-462b-9516-e0832a0c49be)

<div align="center">
 [가을 시작일 예측]

  2030년 : 10월 5일

  2035년 : 10월 5일

  2040년 : 10월 5일
</div>


![winter_date](https://github.com/KDT5NUMPY/KDT-5_NumpyProject/assets/155441547/63cf1861-1ae3-4026-a561-cdafa2b02ce8)

<div align="center">
 [겨울 시작일 예측]

  2030년 : 12월 16일

  2035년 : 12월 15일

  2040년 : 12월 15일
</div>

### (3) 그래프 결과 분석

대구의 4계절 길이에 확실한 변화가 일어나고 있음을 알 수 있다. 봄의 길이는 거의 변화 없으나 약간 증가 추세를 띠었고, 여름의 길이는 확실하게 증가 추세, 가을과 겨울의 길이는 감소 추세를 띤다. 특히 가을의 시작일은 2030년부터 2040년까지 꾸준히 같은 날로 예측되 반면 봄과 여름의 시작일이 더 일러질 것으로 예측되는 것이 봄과 여름이 길어지고 있다는 사실을 뒷받침해준다. 계절 길이 그래프에서 겨울의 길이는 눈에 띠게 감소하지만 가을의 길이는 별반 차이가 없는 것을 보아 온도가 전반적으로 올라가고 있음을 예측할 수 있다.

### (4) 결론

💡 각 계절의 시작일 데이터를 통해 다음 년도 시작일과 다음 년도의 4계절 길이를 예상할 수 있다.
계속해서 봄과 여름이 길어지고 겨울은 짧아지고 있다. 사계절예측은 자연 재해 발생 가능성을 예측하는 데 도움이 된다. 일부 지역에서는 특정 계절에 태풍, 폭우 등의 자연재해가 더 많이 발생한다. 여름이 늘어난 만큼 장마, 폭우와 폭염에 대한 재해 발생 가능성을 예측하고, 이에 대한 대비 및 대응 계획을 수립해야한다.
</details>

<details>
  <summary>
    이승민(황사와 중국 산업화의 상관관계 파악)
  </summary>

</details>

<details>
  <summary>
    권혁원(태풍이 우리나라에 미치는 전반적인 영향)
  </summary>

</details>

<details>
  <summary>
    고우석(강설량, 강설일수와 결빙일수의 상관관계)
  </summary>
