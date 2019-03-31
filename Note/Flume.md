<blockquote><p>Microsoft R Server &amp; Bigdata Analysis 20190306부터~</p>
</blockquote>
<h3>FLUME</h3>
<ul>
<li><p>플룸(Flume)? </p>
<p>	: 로그형, 스트링형 데이터</p>
<p>	: Java로 만들어졌다</p>
<p>	: 응용분야 - 전자상거래(정의된 로그데이터를 Hadoop에서 관리 및 분석), IoT센서로 주기적 발생 로그 저장 분석, 대량의 이벤트성 데이터</p>
</li>
<li><p>신뢰성 : 장애없이 이용할 수 있을 것</p>
</li>
<li><p>확장성(Scalablity) : scale-out 확장 가능한 특성</p>
</li>
<li><p>Scale-up : 한 대의 서버의 성능을 높이기 위해서 사양을 업그레이드 시켜주는 것</p>
</li>
<li><p>Scale-out : (옆으로 증대) 노드를 증가시켜주는것 = 컴퓨터를 증설시키는 것</p>
</li>
<li><p>플룸의 기본 요소</p>
<ul>
<li>소스</li>
<li>채널</li>
<li>싱크</li>

</ul>
</li>

</ul>
<p>&nbsp;</p>
<h3>R</h3>
<ul>
<li><p>주요 특징 : OpenSource, 데이터분석, 강력한 그래프기능, 데이터핸들링, 메모리에서작동(RAM)-inMemory</p>
</li>
<li><p>장점 : R은 GPL이다</p>
</li>
<li><p>단점 : 보안에 굉장히 취약, 메모리의 크기에 영향을 많이 받는다, 한국어기능제공X</p>
</li>
<li><p>주요기능 : 통계분석, 데이터마이닝, 빅데이터분석, GIS, 웹크롤링, 텍스트마이닝, SNA, 기계학습, Shiny를 이용한 웹앱 개발 ... 소프트웨어개발은 불가능하다★</p>
</li>
<li><p>R의 패키지(Package) : 함수, 데이터, 코드, 문서 등의 묶음</p>
<ul>
<li><p>설치 : install.packages(&quot;패키지명&quot;) / install.packages(라이브러리)</p>
<ul>
<li>double-quotation으로 패키지명 설정 및 라이브러리는 quotation-less로 써주어야 한다</li>

</ul>
</li>

</ul>
</li>
<li><p>%/% 몫 , %% 나머지, / 나누기</p>
</li>
<li><p>변수는 벡터형</p>
</li>
<li><p>c() : concatenate, combination</p>
</li>
<li><p>요인(Factor) : 특정 자료를 범주형 자료로 변경해 준다.(벡터는 범주형 자료로 인식하지 못한다.)</p>
</li>
<li><p>행렬(Matrix) : 2차원</p>
</li>
<li><p>배열(Array) : 3차원 이상으로 구성될 수 있다.</p>
</li>
<li><p>리스트(List) : 행렬, 데이터프레임, 배열, 벡터 등 모든 형태를 요소로 가질 수 있다.</p>
</li>
<li><p>조건절 : if / if-else</p>
</li>
<li><p>반복절 : for / while</p>
</li>

</ul>
<p>&nbsp;</p>
<h3>Hadoop</h3>
<ul>
<li>hadoop? </li>
<li>Hadoop의 요소 : Batch process(ResourceManager - NodeManager) + Storage(HDFS : Namenode - DataNode)</li>
<li>YARN : Resource 관리 및 스케쥴링</li>
<li><strong>MapReduce</strong> : Hadoop Batch Shell의 Framework</li>
<li>HDInsight</li>
<li>Zookeeper : 분산코디네이터, 하둡의 에코시스템, 변수를 선언해주고 공유할 수 있게 해주는 시스템</li>
<li>StorageAccount : MS Azure에서 가장 저렴하게 쓸 수 있는 Storage</li>

</ul>
<p>&nbsp;</p>
<h3>Apache Spark</h3>
<ul>
<li><p>종류</p>
<ul>
<li>Spark SQL</li>
<li>Spark Streaming</li>
<li>Spark MLib</li>
<li>GraphX</li>

</ul>
</li>
<li><p>배치프로세싱 + </p>
</li>
<li><p>장점 : In-memory Computing (중간 처리과정을 메모리에서 하기때문에 빠르다.)</p>
</li>
<li><p>RDD : Resilient Distributed Dataset / 분산컬랙션 (내결함성을 가진다 ; 장애생겼을 때 병렬저장되어있는 요소를 가지고와서 다시 쓰는 방식)</p>
</li>
<li><p>RDD 연산 형태 : Transformation + Action</p>
</li>
<li><p>Map-Reduce Coding 실습 </p>
<ul>
<li>e.g.	word count / 0329 Question01-01 (단어빈도수구하기 - spark이용)</li>

</ul>
</li>

</ul>
<p>&nbsp;</p>
<h3>Kafka</h3>
<ul>
<li>브로커가 있다</li>
<li>pub-sub architecture (publisher-subscriber)</li>
<li></li>

</ul>
<p>&nbsp;</p>
