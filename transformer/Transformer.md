[→ Open in Slid](https://app.slid.cc/docs/0b7e319955f54a21a01434cac9e3f942)


---

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/32aaf78e-19b8-47df-93c8-cf566a9febc2.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=3.440619020980835)

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/ccdd40cc-e877-4e1c-bd82-0788e1204549.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=11.545524975204469)


Transformer: 기존 인코더-디코더 모델을 발전시킨 모델

- RNN을 사용하지 않는다.

- RNN기반 인코더-디코더 모델보다 학습이 빠르고 성능이 좋다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/be030659-8d75-4814-8d91-2fa9cf81836b.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=26.564572980926513)

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/b6d10e21-29a0-4f70-94d4-51e128283292.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=38.06709821553039)

- RNN을 사용하지 않기 때문에 학습이 더 빠르다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/674bf733-438f-433c-be91-40ca76ca309a.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=48.14438692752075)


Transformer를 한 단어로 표현하자면 "병렬화" 이다.


일을 최대한 한 방에 처리한다.


RNN이 첫번째 단어부터 마지막 단어까지 순차적으로 계산하여 입력된 단어들을 인코딩 하는 반면 Transformer는 이 과정을 한 방에 처리한다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/57069faf-00c1-46de-8c2e-37bac596b441.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=83.51037710681152)

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/fb967f37-1bf9-45e0-bbd0-a7fda9215043.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=94.00820182833863)

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/be31d37f-a3ab-4418-b405-e22a7a5c5d2e.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=100.82392817166138)


가장 전통적인 인코더-디코더 모델


: 문맥 벡터가 고정된 크기이므로 너무 긴 문장을 저장하기 힘들어 번역 결과가 엉터리가 되는 경우가 많다. 그래서 attention mechanism을 적용한 조금 더 진보된 인코더-디코더 모델이 등장한다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/cf1bddbd-95df-4e0f-81e5-e6faaedbeb6d.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=142.463961)


가장 진보된 점?

- **고정된 크기의 문맥 벡터를 사용하지 않는다!**

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/b3aaaa82-b212-4bf5-af11-8077012aeba1.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=154.7482350782013)

- 대신, 단어를 하나씩 번역할 때마다 인코더 출력값에 동적으로 attention mechanism을 수행하여 효율적으로 번역을 수행한다는 큰 장점이 있다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/3fdb28c9-ec0e-4775-813a-151db096ba81.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=162.876408)

  - **인코더의 모든 상태값을 활용한다.**

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/eaf1f076-b2ae-4397-a702-13f660e2d453.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=172.2134560305176)

  - 동적으로 인코더를 활용하기 때문에, 긴 문장에 대한 번역성능이 이전 인코더-디코더 모델보다 더 나아졌다.


‏‏‎ ‎


\=> Attention mechanism은 기존 인코더-디코더 모델의 성능을 많이 향상시켜서 주목을 받았다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/f69d6d15-edbc-4372-af72-3b0d4836cf12.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=184.6581050152588)

- 여전히, RNN cell을 순차적으로 계산하여 느리다.

- 성능도 더 높일 수 있는 가능성이 충분히 있다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/fa8186da-390a-4d13-b4ea-6322cd6894ea.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=193.51659208773805)


\=> 사람들은 RNN을 대신할 빠르고 성능 좋은 방법을 찾아 고민을 함.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/ea8ced30-fe3f-4862-91cf-6603315f3550.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=197.53703602098082)


\=> Attention만으로도 입력 data에서 중요한 정보들을 찾아내 단어를 인코딩할 수 있지 않을까?

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/4b7ee3bc-6356-4ee8-bfe5-2a560233e5da.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=205.0068220743866)


Attention is all you need!


: RNN에서의 순차적인 계산을 Transformer에서 단순 행렬곱으로 한 번에 처리되게 되었다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/cfa694da-ff41-4e3d-abc5-79c3ba2f3680.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=218.80397508773802)


Transformer는 한 번의 연산으로 모든 중요 정보를 각 단어에 인코딩하게 된다.

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/89a5cc38-429b-46e8-b280-bd9e19a7f1be.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=222.6504560629425)


**Transforemr: RNN을 성공적으로 인코더-디코더에서 제거해냄!**

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/7d779f80-c583-425f-80b3-1041c3f202cb.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=251.4791071296997)

[![Transformer image](https://slid-users-assets-v1-seoul.s3.ap-northeast-2.amazonaws.com/public/capture_images/0b7e319955f54a21a01434cac9e3f942/5f1b2b85-6542-4d3c-9c06-893370cd9219.png)](https://app.slid.cc/vdocs/0b7e319955f54a21a01434cac9e3f942?v=d84c82456c6e4ef9ac0b474d676c1da7&start=273.2505009694824)


RNN이 없는 Transformer는 어떻게 단어의 위치, 순서 정보를 활용할 수 있을까?


‏‏‎ ‎
