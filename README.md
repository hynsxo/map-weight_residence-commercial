# map-weight_residence-commercial
map weight_residence&amp;commercial, python
## UAM 항로설정을 위하여 지역 인구, 토지, 건물 위험도를 반영하여 지역별 가중치 산정
# 단순 고정인구, 유동인구에 비례하여 위험도평가를 작성하기에는 추가적인 데이터수집과 복잡한 모델 튜닝작업이 함께 동반되어야함 따라서 이와관련하여 다음과 같은 아이디어를 제시

- 제주시 인구데이터 (지역, 인구 수, 시 내 비율)
  - 제주시	871.47	100.00 <br>
  대정읍	78.72	9.03 <br>
  남원읍	188.98	21.69 <br>
  성산읍	107.64	12.35 <br>
  안덕면	105.67	12.12 <br>
  표선면	135.19	15.51 <br>
  송산동	4.47	0.51 <br>
  정방동	0.66	0.08 <br>
  중앙동	0.32	0.04 <br>
  천지동	1.83	0.21 <br>
  효돈동	6.62	0.76 <br>
  영천동	46.18	5.30 <br>
  동홍동	14.30	1.64 <br>
  서홍동	13.34	1.53 <br>
  대륜동	22.24	2.55 <br>
  대천동	50.90	5.84 <br>
  중문동	56.69	6.51 <br>
  예래동	37.72	4.33 <br> <br> <br>
  - 서귀포시 871.47	100.00  <br>
  대정읍	78.72	9.03 <br>
  남원읍	188.98	21.69 <br>
  성산읍	107.64	12.35 <br>
  안덕면	105.67	12.12 <br>
  표선면	135.19	15.51 <br>
  송산동	4.47	0.51 <br>
  정방동	0.66	0.08 <br>
  중앙동	0.32	0.04 <br>
  천지동	1.83	0.21 <br>
  효돈동	6.62	0.76 <br>
  영천동	46.18	5.30 <br>
  동홍동	14.30	1.64 <br>
  서홍동	13.34	1.53 <br>
  대륜동	22.24	2.55 <br>
  대천동	50.90	5.84 <br>
  중문동	56.69	6.51 <br>
  예래동	37.72	4.33 <br> <br> <br>


- 제주시 토지데이터
  - 제주도	871.47	100.00 <br>
  대정읍	78.72	9.03 <br>
  남원읍	188.98	21.69 <br>
  성산읍	107.64	12.35 <br>
  안덕면	105.67	12.12 <br>
  표선면	135.19	15.51 <br>
  송산동	4.47	0.51 <br>
  정방동	0.66	0.08 <br>
  중앙동	0.32	0.04 <br>
  천지동	1.83	0.21 <br>
  효돈동	6.62	0.76 <br>
  영천동	46.18	5.30 <br>
  동홍동	14.30	1.64 <br>
  서홍동	13.34	1.53 <br>
  대륜동	22.24	2.55 <br>
  대천동	50.90	5.84 <br>
  중문동	56.69	6.51 <br>
  예래동	37.72	4.33  <br>
  - 서귀포시	871.47	100.00 <br>
  대정읍	78.72	9.03 <br>
  남원읍	188.98	21.69 <br>
  성산읍	107.64	12.35 <br>
  안덕면	105.67	12.12 <br>
  표선면	135.19	15.51 <br>
  송산동	4.47	0.51 <br>
  정방동	0.66	0.08 <br>
  중앙동	0.32	0.04 <br>
  천지동	1.83	0.21 <br>
  효돈동	6.62	0.76 <br>
  영천동	46.18	5.30 <br>
  동홍동	14.30	1.64 <br>
  서홍동	13.34	1.53 <br>
  대륜동	22.24	2.55 <br>
  대천동	50.90	5.84 <br>
  중문동	56.69	6.51 <br>
  예래동	37.72	4.33 <br>
  - 면적기준 안전도
    (2023년 통계)자료를 기반으로
    - 1백 미만: 0.537
    - 1~2백:  0.219
    - 2백~3백: 0.061
    - 3백~5백0.078
    - 5백~1천: 0.061
    - 1천~3천: 0.031
    - 3천~1만: 0.012
    ![land](https://github.com/user-attachments/assets/a282c6de-0785-4d46-bb70-32628cb751a0)



- 제주도의 각 용도별 비율
주거: 0.607 <br>
상업: 0.196 <br>
공업: 0.005 <br> <br> <br>

- 건축물 용도별 안전도
<img width="705" alt="danger" src="https://github.com/user-attachments/assets/e4984b10-20eb-485e-bb28-91ebe5667473">
