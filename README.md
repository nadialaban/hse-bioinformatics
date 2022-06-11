## Проект: Индивидуальная часть
#### Абу Аль Лабан Надя, группа 2

Целью работы над проектом является поиск и изучение консервативных участков генома Z-ДНК в геномах прокариот и эукариот, где в процессе выполнения проекта будут получены важные практические навыки биоинформатика – работа в командной строке с утилитой bedtools, визуализация данных, конвертация координат участков между разными версиями генома (разными организмами) и т.п.  

Введение
---
- **Таксон:** Ascomycetes.  
- **Род:** Kazachstania.  
- **Выбранные виды:**  
  
| # | Вид                              | Сборка          | Общая длина | % GC    | Хромосом | Скаффолдов | Контигов |
|---|----------------------------------|-----------------|-------------|---------|----------|------------|----------|
| 1 | Kazachstania africana CBS 2517   | GCF_000304475.1 | 11,130,140  | 36,3068 | 12       |         12 | 34       |
| 2 | Kazachstania naganishii CBS 8797 | GCA_000348985.1 | 10,845,821  | 45,8879 | 13       |         13 | 95       |
| 3 | Kazachstania barnettii           | GCA_903064755.1 | 12,616,033  |    33,7 | 0        |         14 | 71       |
| 4 | Kazachstania saulgeensis         | GCA_900180425.1 | 12,935,755  |    32,2 | 0        |         17 | 94       |
| 5 | Kazachstania exigua              | GCA_016584175.1 | 13,507,013  |    33,3 | 0        |        588 | 773      |
  
* данные взяты с ncbi  

Тетрадка с решением
---
- [Ссылка](https://colab.research.google.com/drive/1uEgMInf9ucHa5XyDMl-9Dx-WHBQ8-1dG?usp=sharing) на коллаб

Для удобства таблица разбита на несколько

Аннотированные гены
---
| # | Вид                              | Количество аннотированных генов | Доля аннотированных генов | Количество экзонов | Доля экзонов |
|---|----------------------------------|---------------------------------|---------------------------|--------------------|--------------|
| 1 | Kazachstania africana CBS 2517   | 546                             | 0.710668                  | 546                | 0.710668     |
| 2 | Kazachstania naganishii CBS 8797 | 5486                            | 0.740008                  | 5486               | 0.740008     |
| 3 | Kazachstania barnettii           | 5473                            | 0.644475                  | 5473               | 0.644475     |
| 4 | Kazachstania saulgeensis         | 5908                            | 0.646064                  | 5908               | 0.646064     |
| 5 | Kazachstania exigua              | 5522                            | 0.619264                  | 5522               | 0.619264     |

Z-ДНК
---
| # | Вид                              | Количество предсказанных Z-ДНК | Общая длина предсказанных Z-ДНК | Количество предсказанных Z-ДНК с ZH-Score >= 500 | Общая длина предсказанных Z-ДНК с ZH-Score >= 500 |
|---|----------------------------------|--------------------------------|---------------------------------|--------------------------------------------------|---------------------------------------------------|
| 1 | Kazachstania africana CBS 2517   | 421466                         | 3707236                         | 3622                                             | 36414                                             |
| 2 | Kazachstania naganishii CBS 8797 | 504857                         | 4591438                         | 19026                                            | 195766                                            |
| 3 | Kazachstania barnettii           | 123979                         | 10855352                        | 4443                                             | 46960                                             |
| 4 | Kazachstania saulgeensis         | 515417                         | 4477768                         | 6046                                             | 65086                                             |
| 5 | Kazachstania exigua              | 46412                          | 403950                          | 5467                                             | 57602                                             |
  
Гистограммы с распределением ZH-Score можно посмотреть [здесь](https://github.com/nadialaban/hse22_project/tree/main/pictures/zh-score%20histagrams).  
Расположение предсказанных Z-ДНК:  
<img width="1279" alt="image" src="https://user-images.githubusercontent.com/23341597/173169895-8cc47260-1ee4-4e7f-8f68-eefb707734e7.png">  
Для примера в отчете приведен только первый вид и первые 5 предсказаний.  
Остальные примеры можно посмотреть [тут](https://github.com/nadialaban/hse22_project/tree/main/pictures/intersections)  
  
Распределение предсказанных Z-ДНК:  
<img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173204206-95ff0df3-d9e8-4a27-8158-4768c6a8fda8.png">  

Гомологичные кластеры
---
Всего получено 5263 кластера.  
Гистаграмма кластеров по количеству геномов, которые в них входят:  
<img width="390" alt="image" src="https://user-images.githubusercontent.com/23341597/173170100-b1dd191d-e6a8-46da-8210-35d4c4da075d.png">
  
Для работы было отобрано 10 кластеров с самым большим средним ZH-Score:  

<table>
<thead>
  <tr>
    <th>Кластер</th>
    <th>Количество генов</th>
    <th>Вид</th>
    <th>Белок</th>
    <th>Ген</th>
    <th>Средний ZH-Score</th>
    <th>Функция </th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="5">1</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003956363.1</td>
    <td>KAFR_0C02350</td>
    <td>776.676650</td>
    <td>shypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022462785.1</td>
    <td>KNAG_0B00920</td>
    <td>3703.704260</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041403915.1</td>
    <td>KABA2_01S00836</td>
    <td>1089.961633</td>
    <td>Dam1p</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN17962.1</td>
    <td>KASA_0Q03542G</td>
    <td>314233.817167</td>
    <td>similar to Saccharomyces cerevisiae YGR113W DAM1. Essential subunit of the Dam1 complex (aka DASH complex)</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0656389.1</td>
    <td>C6P45_002731</td>
    <td>2115.149238</td>
    <td>DASH complex subunit dam1</td>
  </tr>
  <tr>
    <td rowspan="5">2</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003958880.1</td>
    <td>KAFR_0H03350</td>
    <td>5362.614750</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022465865.1</td>
    <td>KNAG_0H02060</td>
    <td>1508.877027</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041404842.1</td>
    <td>KABA2_02S04840</td>
    <td>1855.924250</td>
    <td>transcription factor TFIIIB subunit BDP1</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN22214.1</td>
    <td>KASA_0I02453G</td>
    <td>10894.720000</td>
    <td>similar to Saccharomyces cerevisiae YNL039W BDP1.  Essential subunit of RNA polymerase III transcription factor (TFIIIB)</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0658649.1</td>
    <td>C6P45_002091</td>
    <td>6923.140347</td>
    <td>Transcription factor TFIIIB component B</td>
  </tr>
  <tr>
    <td rowspan="5">3</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003959711.1</td>
    <td>KAFR_0K02220</td>
    <td>807.699550</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022462890.1</td>
    <td>KNAG_0B02020</td>
    <td>1565.900875</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041404168.1</td>
    <td>KABA2_01S06688</td>
    <td>1085.165333</td>
    <td>uncharacterized protein</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN18212.1</td>
    <td>KASA_0Q06523G</td>
    <td>7228.061900</td>
    <td>similar to Saccharomyces cerevisiae YHR066W SSF1. Constituent of 66S pre-ribosomal particles, required for ribosomal large subunit maturation</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0657277.1</td>
    <td>C6P45_002457</td>
    <td>7931.176058</td>
    <td>rRNA-binding ribosome biosynthesis protein</td>
  </tr>
  <tr>
    <td rowspan="5">4</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003955828.1</td>
    <td>KAFR_0B03970</td>
    <td>8650.887500</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022466351.1</td>
    <td>KNAG_0J00230</td>
    <td>1545.554825</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041404660.1</td>
    <td>KABA2_02S00572</td>
    <td>4089.099989</td>
    <td>Aep2p</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN22028.1</td>
    <td>KASA_0I00264G</td>
    <td>35313.342725</td>
    <td>similar to Saccharomyces cerevisiae YMR282C AEP2. Mitochondrial protein, likely involved in translation of the mitochondrial OLI1 mRNA</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0671161.1</td>
    <td>C6P45_001174</td>
    <td>4553.600027</td>
    <td>ATPase expression protein</td>
  </tr>
  <tr>
    <td rowspan="5">5</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003958594.1</td>
    <td>KAFR_0H00500</td>
    <td>1033.33100</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022463970.1</td>
    <td>KNAG_0C06290</td>
    <td>783.82300</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041407865.1</td>
    <td>KABA2_08S01452</td>
    <td>767.29470</td>
    <td>type II protein arginine methyltransferase</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN22275.1</td>
    <td>KASA_0H00550G</td>
    <td>64846.38700</td>
    <td>similar to Saccharomyces cerevisiae YKL162C. Putative protein of unknown function</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0656741.1</td>
    <td>C6P45_002626</td>
    <td>1379.64074</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td rowspan="5">6</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003956185.1</td>
    <td>KAFR_0C00550</td>
    <td>1165.102067</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022466418.1</td>
    <td>KNAG_0J00910</td>
    <td>1992.403556</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041407085.1</td>
    <td>KABA2_06S00946</td>
    <td>4761.159467</td>
    <td>uncharacterized protein</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN21413.1</td>
    <td>KASA_0K00594G</td>
    <td>1838.019950</td>
    <td>similar to Saccharomyces cerevisiae YBR050C REG2. Regulatory subunit of the Glc7p type-1 protein phosphatase</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0655022.1</td>
    <td>C6P45_003206</td>
    <td>8676.699851</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td rowspan="5">7</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003957699.1</td>
    <td>KAFR_0E04130</td>
    <td>4139.407940</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022463313.1</td>
    <td>KNAG_0B06390</td>
    <td>2534.241900</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041408366.1</td>
    <td>KABA2_10S01034</td>
    <td>15683.591160</td>
    <td>ornithine-oxo-acid transaminase</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN21966.1</td>
    <td>KASA_0J03201G</td>
    <td>3407.397267</td>
    <td>similar to Saccharomyces cerevisiae YLR438W CAR2 L-ornithine transaminase (OTAse)</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0663124.1</td>
    <td>C6P45_000903</td>
    <td>7887.106448</td>
    <td>ornithine aminotransferase</td>
  </tr>
  <tr>
    <td rowspan="5">8</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003955962.1</td>
    <td>KAFR_0B05320</td>
    <td>742.133800</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022465966.1</td>
    <td>KNAG_0H03060</td>
    <td>2463.227111</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041407562.1</td>
    <td>KABA2_07S02904</td>
    <td>930.778775</td>
    <td>putative hydrolase</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN21125.1</td>
    <td>KASA_0L01529G</td>
    <td>802.507175</td>
    <td>similar to Saccharomyces cerevisiae YDR101C ARX1. Shuttling pre-60S factor</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0661944.1</td>
    <td>C6P45_001233</td>
    <td>7576.153970</td>
    <td>putative metalloprotease arx1</td>
  </tr>
  <tr>
    <td rowspan="5">9</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003954718.1</td>
    <td>KAFR_0A01450</td>
    <td>924.779300</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022462870.1</td>
    <td>KNAG_0B01810</td>
    <td>2015.605109</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041408799.1</td>
    <td>KABA2_12S03146</td>
    <td>1726.483129</td>
    <td>DNA helicase SRS2</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN21722.1</td>
    <td>KASA_0J00198G</td>
    <td>631.851667</td>
    <td>similar to Saccharomyces cerevisiae YJL092W SRS2 DNA helicase and DNA-dependent ATPase involved in DNA repair</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0668030.1</td>
    <td>C6P45_005120</td>
    <td>6620.833000</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td rowspan="5">10</td>
    <td rowspan="5">5</td>
    <td>Kazachstania africana CBS 2517</td>
    <td>XP_003957646.1</td>
    <td>KAFR_0E03600</td>
    <td>731.28430</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania naganishii CBS 8797</td>
    <td>XP_022463809.1</td>
    <td>KNAG_0C04610</td>
    <td>2541.41200</td>
    <td>hypothetical protein</td>
  </tr>
  <tr>
    <td>Kazachstania barnettii</td>
    <td>XP_041405574.1</td>
    <td>KABA2_03S04026</td>
    <td>69753.76425</td>
    <td>Pno1p</td>
  </tr>
  <tr>
    <td>Kazachstania saulgeensis</td>
    <td>SMN19646.1</td>
    <td>KASA_0O02101G</td>
    <td>825.09980</td>
    <td>similar to Saccharomyces cerevisiae YOR145C PNO1 Essential nucleolar protein required for pre-18S rRNA processing</td>
  </tr>
  <tr>
    <td>Kazachstania exigua</td>
    <td>KAG0667900.1</td>
    <td>C6P45_005223</td>
    <td>3951.01970</td>
    <td>pre-rRNA-processing protein pno1</td>
  </tr>
</tbody>
</table>
 * *В качестве функции взят атрибут*  `product` *из gbff*

    
Распределение Z-ДНК относительно генов в кластере:  
| Кластер       | 1                                                                                                                                         | 2                                                                                                                                         | 3                                                                                                                                         | 4                                                                                                                                         | 5                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Распределение | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173205855-d99a0932-61fc-4de3-8db9-fe2dc6c7c433.png"> | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173205879-dec8d975-695f-4529-8182-5cc4d82a2517.png"> | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173205895-ee73ae9d-3aa8-4204-9641-545bb2c22b80.png"> | <img width="541" alt="image" src="https://user-images.githubusercontent.com/23341597/173205908-0423daf5-58c7-4e12-bdb4-94496959890b.png"> | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173205939-305030f8-0fab-457c-88f1-efb60ae2fffc.png"> |
| Кластер       | 6                                                                                                                                         | 7                                                                                                                                         | 8                                                                                                                                         | 9                                                                                                                                         | 10                                                                                                                                        |
| Распределение | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173205988-de470ee1-a157-4ab5-bed3-9d8313ec14ac.png"> | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173206046-3d660b16-7bac-476d-ba04-dbecc7f5b30b.png"> | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173206075-f51b185a-238d-419a-9d0c-36230e545304.png"> | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173206102-1449bea0-c488-4e60-8168-bb8ac8487824.png"> | <img width="540" alt="image" src="https://user-images.githubusercontent.com/23341597/173206119-fb6bfed9-f25e-43eb-8e7a-ebd3f923661b.png"> |  
  
Располодение Z-ДНК относительно генов можно посмотреть [тут](https://github.com/nadialaban/hse22_project/tree/main/pictures/clusters_distribution)

Множественное белковое выравнивание
---
Производилось с помощью `muscle`

<details>
  <summary>Кластер # 1</summary>
    
  ```  
  >KAG0656389.1 DASH complex subunit dam1 [Kazachstania exigua]
MSEARNNESSSRTGTDYKLSVSSNPGSRRSSIASVNGAESFT--TGG--TNGTGFDMDGEQNVLKEYLVPQIRELTDSIV   
TLDSNMIRLNVIHDNLVDFNESFGSLLYGILCTSACTDFPGVPSDIERELRGIKHLQTLKQERLQLEKELFSLKSRT-MN  
TTDKRT--------ASGKFPEPLFPARGTIS----------------N----NIPRRRSTNRN---------DNDISKGI  
IYDDNNSEESFILNPPMQRTSTSISSQKQAPNRRSVSMND-ASKQSSKLRRRSILHTIRNSLLEDERG-NPRLNSGTASR  
EIG-SNGTARPSVVG-APTRNIGRPISTDTARRNT-YSTGGNKIESS--NRVNRTRTSTKPKSIKDRPPFR  
>XP_022462785.1 hypothetical protein KNAG_0B00920 [Kazachstania naganishii CBS 8797]  
MSEFQPNKS---SGTEYRLSVSSNPNSRRSSLVGHK--DTYNTRASSLPHDGKANFEDDDANLLDKYLRPQLNDLHDSVV  
TMDDNFLRLNNIHENLVDLNESFGSLLYGIIVNSACINFAGFPTDTREQLEVAKALHSIQQEKRALLEELDALQKPETVK  
PGSSNSGVNSGTGVKRGQFSQPIFTTAQAKRITAKSNGRGVVKRAATDNQRNRFSRTRYNDENSNRQATT-A-GTADADN  
DDDDNSSEASFVLNPGRDDQSQ-----------YTFD-DSGTANPSRKMRRKSVLNVVRNSVNTNERPPQLARRSHTMG-  
PQPSRAPDGRRSIGGRGPMRRVHNPAAAP-----S--GPAPGPRNSV--QGNTAVRTTSRPKSIDKRPPFR  
>XP_003956363.1 hypothetical protein KAFR_0C02350 [Kazachstania africana CBS 2517]  
MDE-----EKSRTGTEYRLSVSSNPGSRRSSFGSNNDGTSYN-------DDMTAAVNETEQNVLQEYLVPQIRELSDSMI  
TLDDNFIRLNEIHNSLVNLNESFGSLIYGMMCISACIDFPGIPYNVEKELRSMKRLQALKIERESLTKELEELKKPNKQA  
VND-------------SKFVVPHFPPTQLNKRL-------------EK----NGPRSVSENRN--RHFAQPKSNKDQTGG  
DDDDTNSEASFVMNPLVKPP------PNYRDSNHEIR-NEDKRDNTSRLRRKSILHTIRNSLSAEHTS-STNI-------  
-------FSTEERRE-KPTSSATRIP-SPKKRKNPLFQANSRNIASANMNRVNKRKTERKPVPMDKRPPFR  
>XP_041403915.1 Dam1p [Kazachstania barnettii]  
MSEIRNNESSSRTGTEYKLSVSSNPGSRRSSIASININDNFNGKPGN--VNGSGFEMEGDQNVLQEYLVPQIRELTDSVV  
TLDSNLARLNAIHDNLIDLNESFGSLIYGILCTSACTDFPGVSLDIERELRSIKRVQTLKQERLQLEEQLHLLNTNSSVK  
VNISKS--------GSGKFSEPLFPVRGNTTNY------------KTN----NVPRRRFAKNN----------NSTENEN  
VYDDNNSEESFVLNPPIQKQASSVGNPSYAMNQRPVG-NS-TSRQSGKLRRRSILHTIRNSLLVDDNAGYLRPTNN----  
MRN-SNNLERPSLGG-LPTRNIDRVV-QEGPRRKT-FSAASKNNETS--RRVTKIRPQSKSKSINGRPPFR  
>SMN17962.1 similar to Saccharomyces cerevisiae YGR113W DAM1 Essential subunit of the Dam1 complex (aka DASH complex) [Kazachstania saulgeensis]  
MSEIKNNESSSRTGTEYKLSVSSNPGSRRSSIASINVNDNINGRTGN--VNGGGFEKEGDQNVLQEYLVPQIRELTDSIV  
TLDSNLARLNTIHDNLIDLNESFGSLIYGILCTSACTDFPGVSLDIERELRAIKRVQTLQQERLQLEEQLHSLKTRSSLS  
TNNSKP--------SSGKFSEPLFPARGTTTNY------------RTY----NVPRRRSTKNN----------NNPENEN  
IYDDNNSEESFVLNPPVQKQVSSIGNPGYATKQRSMA-NS-NSKQSGKLRRRSILHTIRNSLLVDDNVGNQRSNNN----  
PRG-SNNLERPSLGG-LPTRNIDRTA-QEGPRRNT-FSAAFKNNESS--RRVTKIRPQSKPKSINERPPFR  
  ```
</details>  
  
<details>
  <summary>Кластер # 2</summary>
    
  ```  
>KAG0658649.1 Transcription factor TFIIIB component B [Kazachstania exigua]
MSSVVNKGGTRFAPKIRQRRTATSVP-PVVN---VPTAKSIIS-----KEIDDGEKEEAISTDTVDEGATQVTTQILPND
L-DDNEDLLSKAS---------GDIGPKDIVSKTNDDMGDNAATQVDNNEN-------------------------DKQ-
ESISLLGLSG-KPQRRFSRLPSLSGNM-----GNPLIKPTST--------AQ-NNSNRRLSTIAKNAK-----RKK-VSM
NKLLTE-NEDDATLNAIKKRRLSRTAPPATRKGRTAKKISIISKISVPTESTSDNDEVNEKRKN--SNEDISTDIVPNDG
EYFETYLVRSLEEVPGDVTITDSARYLVDDENFTMDQLCGRTLPIGQISENYDKARKAEKRRLMKRKERRSLRKRAREEF
RSLKSLNKEEEELEREERRKNREKLLNADIPESGPPK-GQQMQLKIGADGKMILDEESTVVDRHKNANLENSQKEKVDEN
PFENLYNNASYGKAQYSDPWSLDEIIKLYKALAMWGTDFNLISQMFPYRTRRQVKAKFSNEERKHPIMIELALRAKLPPS
FDSYCTDIRKELGTIDDFNKKMEQIQVDHEKNIQEIEKAKESAKLEDMNNQKEGD----LDKKSSGGFRKKFLNTYRKSE
VVLGTIDDVKKLRKITDESIKEE---------------------------------------------GEHGSEEEEEEE
EEEEEEEEEANEDEKEAKEEEKEVHNEDKEEEQAEDNKVDKASEETT----KDKSTEKD
>XP_003958880.1 hypothetical protein KAFR_0H03350 [Kazachstania africana CBS 2517]
MSSVVNKSGTRFAPKVRQRRTATASPVPLLTQR-LPAKTNVIE-----DKPSDVEKSNSD----------------REDD
MHDREDRALVRGNEEDAKVSISMDVSPVEKPS----------------------------TLSRDELF----TFLDTST-
QRS---K-PH-VVQARSSRLNSLTHHLLGTIDAKPVFKPSYN--------EMTVPPTRRLSTISNGNRNPNTLPRR-IRI
NSLLDNASPNDDTLRSIKKRRKSSA---SRRKSTSTHRLSVVSKIKRDPALDTD-------------------GIYDRNG
NVHDPFKIRSIKDLPKKIEEKDSSRYTIDESIFTMADLCKPTLPIGEISDNFERANQATRSKLEKRKKRRELRQKAREDF
KSLQALNKEEDERLKQERKEAAEKFLNRDVPEYQETP-TQGIKLKLNPDGQINVDEESTVVDRHKNASLENAHKEKVDEN
PFENLYNYGTYGKGSYTDPWKTEELIKFYKALSMWGTDFNVISQLFPYRTRRQIKSKFISEEKKHPVMVELALRSKLPPD
FVQYCTDIKKEIGTVDDFNKKIEELQINHENNLKELERAKENAKLEDIKTQNELE-NSPINKKSAGGLMSNDLKNYRKSE
VVLGTIDDIKRQREET---A------------------------------------------------------------
--------KK------------------------------EEDDEND----GDVSTAAE
>XP_022465865.1 hypothetical protein KNAG_0H02060 [Kazachstania naganishii CBS 8797]
MSSVVNKSGTRFTPRLKGRRAPVAAA-V-TK---EPSSSVVNTQETVTEPLIEKPSPL-IEKPSVNELE--GATQVPEAN
F-ESDEEE---RKEE-------EDIDDRLEER-----TVPIRTTASTKNASGIKKSNAPVSLSGQPIFDKSFMPSQTSTQ
VPPGIHGISVNHPTLRSSRLRSLSKNL-----EKPHFKPSFNEGRKNSVSSP-TTTRRRLSSISNNLP-----R-T-LK-
NGQVIE-SEN-SALNTLKRRRLSTRT-NISKKSGSTHRISIVPKIQAPVKKAVKLPDPI-------ARKKGESDLYGRTD
EMYEKYQVKNSKEIPKNMKVEDSAKYLIDEDCFTMAELCKRTLAIGEVSDNFERAQEARRMKLEKRKQRRELRMKARDQF
KSLQDLTKEEVEREKEERKQKRDKLLNSEFPEDQYRQSTNAPQLKLNKHGDIGLDEESTVVDRHKNATLDNFQKQKVDEN
PFDNLYNYGTYGRATYTEPWTPDEMVKFYKALAMWGTDFNLLAELFPYRTRRQVKSKFTNEETKHPVMIELALRSKLPPD
FDSYCKETRKDLGTVESFNEKVEALQKAHAQNLKELEKAKELASLEDLNNNKDGDTKSLINKKTSGGLFSRELKSYRKGE
VVLGTIDDAKRKRELE-ESISEIPAAEDEEVTSRIEDTEVAQQTNGNEKEHTETEPSESGPADPKLSEGQKDTPANDETE
-QS-GAELGK------------------------------EGTEQGN----SEKPTDAE
>XP_041404842.1 transcription factor TFIIIB subunit BDP1 [Kazachstania barnettii]
MSSVVNKGGTRFAPKMRQRRTAASGS-PAVGSIATPVISIQPT-----KEVDDIG------NGEVNDSATLVATQVTTQD
L-DGDEGPLAKGTQE-------EDVDPKQVIN--------------------------------------------TEE-
KRLSISGPTD-RHQRRFSRLPSLSGTL-----GSPLLKPSLA--------GS-NNTNRRLSTISKNPK-----KKKILSM
NKLLSE-NEDDATLNAIKKRRLSRTVPPATRRSKSSRKSSVISKIFVPQEAHSEEDEEGDNLK---DRRDSMTDTVPNDG
EYFETYIVRNIDEVPADVTITDSARYLVDDEHFTMDQLCKRTLPIGQISENFDKARNAEKQKILKRKERHNLRKRAREEF
KSLQSLNKEEEDLEKEEWKKNREKLLNAEIPEFGAPK-GQQMQLKIGADGKMILDEESTVVDRHRNANLENAQKEKLDEN
PFENLYNNASYGKSTYTDPWTLDEIIKLYKALAMWGTDFNLISQMFPYRTRKQVKAKFVNEERKHPIIIELALRAKLPAN
FDVYCTDIRKELGTVDDFNEKMAQIQSDHEKNIQEIEKAKESAKIEDMNIQKDGD----LDKKSSGGFRKKYLNTYRKSE
VVLGTIDDVKKLRKIKDDAVKEE---------------------------------------------GEEDKSDNDEEE
KED-GEE-DR------------------------------EEEEEKEGDLSKESIDEKK
>SMN22214.1 similar to Saccharomyces cerevisiae YNL039W BDP1 Essential subunit of RNA polymerase III transcription factor (TFIIIB) [Kazachstania saulgeensis]
MSSVVNKGGTRFAPKMRQRRTAASGL-PTVGAVATPITAVQAS-----EEVDDAGKDE-ISKSVVNDSATLVATQISTQE
V-DVDEGPLAKGTQN-------EDIDPKQIIN--------------------------------------------TDG-
KRLSVSGPSD-KHQRRFSRLPSLSGTL-----GSPLLKPSLT--------GP-NNTNRRLSTISKNPK-----KKKILSI
NKLLSE-NEDDATLNAIKKRRLSRTAPPATRRSKSGRKSSVISKIFVPQETNSDGEEDGDTLRNNRERKDSITDTVPNDG
EYFETYLVRSIDEVPADVTITDSARYLVDEDNFTMEQLCKKTLPIGQISENFDKARNAEKQNLLKRKERRNLRKRAREEF
KSLQSLNKEEEELEKEERKKKREKLLNAEVPEFGAPK-GQQMQLKIGADGKMILDEESTVVDRHRNANLENAQKEKVDEN
PFENLYNNASYGKGTYTDPWTLDEIIKLYKALAMWGTDFNLISQMFPYRTRKQVKAKFVNEERKHPIMIELALRAKLPAD
FDVYCVDIQKELGTVDDFNKKIAQLQIDHEKNIQEIEKARESAKIEDMNIQRDGD----MDKKSSGGFRQRYLNTYRKSE
VVLGTIDDVKKLRKIKDETVKEE---------------------------------------------GEGKGEDEHDGS
EHD-SEEAEA------------------------------EEEEQQE----EEDANEKK

  ```
</details> 
  
<details>
  <summary>Кластер # 3</summary>
    
  ```  
>SMN18212.1 similar to Saccharomyces cerevisiae YHR066W SSF1 Constituent of 66S pre-ribosomal particles, required for ribosomal large subunit maturation [Kazachstania saulgeensis]
MARRRTKKRTHVQPTADALKGIPKSMVIRVGQTSLANHALNQLVKDFRQIMQPHTAIRLKERKSNKLKDFVVMCGPLDVS
HLFIFTQSEKTGNVSLKVARTPNGPTITFQVQDYSLSKDIKKYLKKPKSLNSEDVLSPPLLVMNGFNNKLTQNDDADEKD
EKKKVEKIVVSMFQNIFPPLNPSQTHLNSIKRVFMINKDAKTGEISLRHYFIEIKDVEISKSLKSLFKAKSNPNKKLPVL
TGKQDISSLILDHDIDPYTSESEVDEQDPDSIISVMEKNKGNLESKIS------IKQKIDREKQKEEQKRQ-KELDIATG
LSTNNEGHAKVED-EGESTNGTDGNINLDENLGNPKKKAIRLTEVGPRLTLKLVKLEEGICSGKVLYHEYVHKTDAEIKK
LEKRHLAKMRLKEERRKEQEANIARKKAVKDAKKERKMERRAARKALEKDAEGDEKMDGDK------------SAESDDD
SDS-NSDSEHNYSDVPEDIDSDLFSDLEEATQ
>XP_003959711.1 hypothetical protein KAFR_0K02220 [Kazachstania africana CBS 2517]
MAKRRTKKRTHVVQSKDELKGIPKSMVIRVGQTSLSNHSLNQLIKDFRQIMQPHTAVRLKERKSNKLKDFIVMCGPLDVS
HLFIFTQSEKTGNVSLKIARTPNGPTVTFNVVDYSLSKDIKRFLRRPKTLAKEDVLDPPLLVLNGFNTN-------SDDD
ESNNVEKVVLSMFQNIFPPLNPSQTQLSSIRRVFMINKDPKTNEISMRHYFINIKDVEISKNLKRLYKAKDHLNKSVPNL
STKQDISSLILDHDLGAYTSESEVED---DSIVKVMDND--NNTTRVN------NQ-----------RKPQ-EPIGEDDG
E----E-EEEEED--Q-------DSMPVAKPVANPKKKAIRLTEVGPRLNLKLIKIEDGICSGKVLHHEFVKKTDAEIKA
LEKRHREKQRLKEQRRKEQEENIARKKATKDAKKQRKLERRKLREEQENELFDGKKEDNDE------------VAKNDES
SESSDSDSD-HYSDVPEDIDSDLFSEVEEA-M
>XP_041404168.1 uncharacterized protein KABA2_01S06688 [Kazachstania barnettii]
MARRRTKKRTHVQPTADDLKGIPKSMVIRVGQTSLANHALNQLVKDFRQIMQPHTAIRLKERKSNKLKDFVVMCGPLDVS
HLFIFTQSEKTGNVSLKVARTPNGPTITFQVQDYSLSKDIKKYLKKPKSLNSEDVLSPPLLVMNGFNNKFTQGDDEDEKD
EKKRVEKIVVSMFQNIFPPLNPSQTQLNSIKRVFMINKDAKTGEISLRHYFIEIKDVEISKSLKSLFKAKSNPNKKLPVL
TGKQDISSLILDHDIDPYTSESEIDEQDPDNIINVMETTKGNSDSKIS------IKQKIDKEKLKEEQKRQ-KELDIATG
LPSNNEEQAKIENEEGESTNGTDGNINLDENLGNPKKKAIRLTEVGPRLTLKLVKLEEGICSGKVLYHEYVHKTDTEIKK
LEKRHLAKLRLKEERRKEQEANIARKKAVKDAKKERKLERRAARKALEKDAEGDEKMEGDD------------NSESDDS
GES-DNDSEHNYSDVPEDIDSDLFSDLEDAAQ
>XP_022462890.1 hypothetical protein KNAG_0B02020 [Kazachstania naganishii CBS 8797]
MAKRRSKKRTHVAPTPESQKGIPKSMVIRVGQTSLANHSLNQLVKDFRNIMQPHTAIKLKERKSNKLKDFVVMCGPLAVS
HLFIFTQSEKTGNVSLKVARTPQGPTITFNVIDYSLGKDIKKFLKRPKSLNNEDLLNPPLLVLNGFSTKN-----KNEDD
PNANVEKIIISMFQNIFPPLNPQTTQLNSIKRVMMLNKDPVTKEISLRHYFIDVKDVDISRNLRKLYTAKSHLNKTVPNL
NRKKDISSLILDHDLGAYTSESEVDDE--EAIVNINESYGKNKNGQIS------VE----------KRKKEKPAIDLETG
LEKDEL-DVEMEE--A-------ATRDAAQPEALPRKKAIRLTEVGPRMNLKLVKIEEGICAGKILHHEYVHKTDQEIKM
LERKHAAKMRLKEQRRKEQEANISKKKAVKDAKKERKLERRRLRKEQ---AEADGKAD------------------NDSS
EGSSESESE-NYDDVPEDIDSDLLSEVEDA-V
>KAG0657277.1 rRNA-binding ribosome biosynthesis protein [Kazachstania exigua]
MARRRTKKRTHVQPDQDTLKGIPKSMVIRVGQTSLANHSLNQLVKDFRQIMQPHTAIRLKERKSNKLKDFIVMCGPLDVS
HLFIFTQSEKTGNVSLKVARTPNGPTITFQVMDYSLSKDIKKFLKRPKSLNGEDVLSPPLLVMNGFNNNFTQ-DETNEDD
SKKQMEKIVVSMFQNIFPPLNPSQTHLNSIKRVFMINKDPKTNEISLRHYFIEIKDVEISKNLKSLFKAKNHLNHKLPVL
TGKKDIASLILDHDIDPYTSESEVDEQDPDNIINVIETDNQNNNNKNNNNNKNTLKLKIEQE----KQKRE-KDMDVATG
LTTEEE-NKDIED--N-------IDNEFEESTSNPKKKAIRLTEVGPRLTLKLVKLEEGICSGKVLYHEYIHKTDSEIKM
LEKKHAAKMKLKEERRKEQEANIARKKAVKDAKKERKLERRAARKAAEKDAEGDENMEKDSDKNNNNNNNNNNSSSNSSS
SDS-ENDSEHNYSDVPEDIDSDLFSDLEDAEQ

  ```
</details> 
  
<details>
  <summary>Кластер # 4</summary>
    
  ```  
>SMN22028.1 similar to Saccharomyces cerevisiae YMR282C AEP2 Mitochondrial protein, likely involved in translation of the mitochondrial OLI1 mRNA [Kazachstania saulgeensis]
MLFRS------------RPVVASKGITNLASQNVLYFPKEMTLNGPFQTH-RFYK-TESTGNASSSKL------------
-------IVNGITKKYG-----DFSKYLDEM------------------------------SRVKVIPNKTGFIKNLDQV
YYEYQGIM-NQSQQLDSLKLRDTNLFLDMFLKLGRLKRAHDVLTDLIKLDGSLVFGDARDIATVRNYLKVRCGS-FSEMW
YTDRAYEIIDNTYIFNLLD-YSLKNNFSYWDTEICYSLGKMNRIELLNKFTMKKWGISIQGPHFIDGE-------IYKAP
NSEVVIALMKIICYIYSD-GMHEANKFLNALIERYPKINLNINFWRHLVLEGSSPKRGNKNFAVGNENGLDGWNTMKQWY
LMRGKTIPFDYSIVEELYRIFERTKNLKDCIAVYTSCFSEFYEQRNKINNNEWSIINKYQKFIVRRLVNKKNYNKVEEFI
TQWSIDSDNERMLRKFSSY-----LIVLKNNKQTNKSYDEMVDD-DMILGSLW
>KAG0671161.1 ATPase expression protein [Kazachstania exigua]
MLGRS------------RLVFCENAIPNIRNAKRI-LP--LAVKFPIAT--RYY----TTAPVSQSDL------------
-------AINGVTQKYA-----EFSTYLDEL------------------------------SKVRPIYNKANLIKNLDQI
YAEYQKILQNPDTRLNSLKLHDTNVTLSMFLKLHRLKRAHNVLTDLIHMDESLVFGESRDIDTVRSYLNVRCGA-YVDMW
YSERSYIVIDNTYVFDLIE-YSLKNGLSYWDSEICYALSKSNQLNLLNQFTMKKWNISINESIIDVQQ-------GMVPP
SSEVIVTLMRIIRYIYKD-GTEEANRFLNNITKQYPTMNLNINFWRNLLLEGSSPLRGNTHFKTGNENGLNNWRTMKEWY
TMRNKQIPFDNSITRELYRVVERTKKIKDCIDIYTNCFSEFYNQRNKITKAEWSIINKYQKFILRRLINKKNSKRTEDFI
TQWSIDNENEKMLRNFVNY-----LTLLKNKKKVTQKYDEMIED-DMILGPLW
>XP_041404660.1 Aep2p [Kazachstania barnettii]
MLLRS------------QPVAASKAITDFASLRVSYFSRDIARGSSFQTH-RLYR-TESSSKTSNSKP------------
-------IVNGIPSKYA-----DFSKNLDEM------------------------------SKYKFIPNKTDFIKNLDQV
YYEYQGIM-NQSQELDALKLRDTNLFLGMFLKLGRLKRAHDVLTDLIQLDESLVFGEARDIDTVRNYLKVRCGS-YSNLW
YGDRSYEITDDTYIFNLID-YSLQNKFSYWDTEICYTLGRMNRIELLNKFTTKKWGISIQGPDFVSGE-------VHKAP
NSEVVTALMKVICYIYSD-GMHEANKFLNGILEKHPNINLDINFWRQLMLEGCSPKRGNKDFAVGNENGLDCWNTMKQWH
NMRRRTIPFDYSITKELYRILERTKNLKDCIAVYTNCFTEFYEQRNKIENSEWSIICKYQKFIIRRLINKKKYSKTEEFI
TQWSLDSGNEAMLRKFSSY-----LIVLKNNKKTNENYDEMVDD-DTILGPLW
>XP_003955828.1 hypothetical protein KAFR_0B03970 [Kazachstania africana CBS 2517]
MERQEVRALYRRVGYMFRPTQCSSYTTTIQSKQ-------LTLGELIQK-----R-QESYNNKSLCMPFEVPKIELRIKT
PKELDAEIQEIITSMHATIDLNRFARLINI---------------------------AL-SEKYNIQRIKERRPEIIFQL
FETYVKLI-SSHEELTILQVEDMNKFINYFVEFKQLKKAQLVMKYLILKSPR-V-LEKYDVSTTRNYLKLNCGA-CHELW
YTNYKIFDFNNTTLDKLVK-YSLDNKIGYWDVEIIHSLGYSGRIRSLEDYILKKWGISLCDRAQVN-T-------TNEAP
ESEVLEAIIN--GFFYRDKRMFRAIKILNEFVNVYPDLNLKITFWKTFMN--NCIKEWDEKVDQKGVVIVEYWETMKRWY
TVHNRRIPFNINFLKVMRTCFKKNNNLVLATDIFQNCFHNFYFCATRMNDSELNVIKEYQNFILSRLIEKKGFSNALTFI
NDHCFSLENKRQLMNYYHGRKEHKLKKMTRNENLEKTYDDMVEE-DFIIGKLW
>XP_022466351.1 hypothetical protein KNAG_0J00230 [Kazachstania naganishii CBS 8797]
MLSMLS-----------RSPVW-LKIPTVTCNRVGYST----LRETLQTKNRLINDTVNPQENSQGPN------------
-------IHKCVTNKYP------ASNNLSELLDLLAGHNVFNILSPTAMQFSVLLNRVLASQNYRHLDSKEN-VEKFFAI
FMRYKGAIALQSNKLTQIQLHDFNLMCDYFIACNQLKKAQLIMDFLLQQDV------KFDVFMIKNYTKLRCGSSFGKQT
LNNKAYKVFDQNTVFQLIGKVEADRKFAFWNNEIVSSLGYTNNITLMEIYIWDLWRISIHDHSTENIKIDHLQQGDAMYP
SSKVLATIVS--SYARHDQTMKRAVDIVERFAKSYPKLLLNVHFWSTLLN--CAIKCGGSKD---PSQFLACWNLMKKWH
TQRSKLMPFQSALLVTILRYMRQTSNLHGTVDILQYWLGPLYLKRGNIPEFERDVLIKYQKQILRKLVDKRKYNWCTAFI
DQWSIDASNKEDLEAFYESR----VDVRESKTRREKAYDDMDDDEDMIIGRLW

  ```
</details> 
  
<details>
  <summary>Кластер # 5</summary>
    
  ```  
>KAG0656741.1 hypothetical protein C6P45_002626 [Kazachstania exigua]
ML-----------------------------------------RLQS-SMR-WKHTDAIPFRDFIEQHNRKYIMKRQ-NF
FSGHMQLNQSNP-LSENLIDYDPILTQCMARWLWLNYKITDYPYHDLNILNIFTDLPQAIYFMRRIMQYFHDILPSESFE
RINYYLFPLYRCDKIN---ERNLLDDIPGNVRIMEDMTLFPM---NKTIDFN--D--KTNNVYINDPMQILMFNDILGNL
SHDLVKYHDVTQQWEQCYIEEETIKNMNERYFDNELDYWCDNTIRQLFDIDFTDQIQRNK-------NLHNEIFIPTQFI
QLLEQLKLYVPDFRLFIIDSPGKKTDTFYSR-LRDFLG-------YTRIGTSKILEPYDNWWVHNCSSEDQ-EK---NIN
SCITFQPDFNHLEKILTNVSENDTRYGFLKPCEIETLGEFCDKWVDHKLKETKMSVTISQDNNSIPTEFLQKLKLQLDLA
TKSSLNILH-S
>XP_022463970.1 hypothetical protein KNAG_0C06290 [Kazachstania naganishii CBS 8797]
MEFTVIRDADWQVVAEGMRTMQLKPAIRIISSWKRFSTLPCGVRPDGGVHPGQRSSSEVIFREYVEKLNKPRVMVRN-RT
FEPR---YTHR--EWKVLRPYEQVIGSCLAKWLWVNYQINDFPYYDLNIVQVFTDLRACTSMCKSIMTFFEKKLSKNHFE
KIHYILVPLYKLDKIP----SAIMDGIPGHVELVNDIKKSPF---HKTGGKLGAL--QSLENWIQDPVYVLFLNDILRNI
AHDLVRFGD--RGWEQCYVCLDNDGQPRDYQFHENPDPLCQRTLDTIFESGS-MG------------YPTQNVYVPSQLI
QLFDVMQSLIPEYRLFAIDHDPTATRTGYTRWLQDIIY-------GTLKTTPGP-----------LETL-L-EG---GHK
LPIQFQPDFKFLNSLYTNLENSKFA---NKMCEVTFLRHFVNDWTDTSASQSS------------------QMQEQYKSL
QGSPLTVLQAA
>XP_003958594.1 hypothetical protein KAFR_0H00500 [Kazachstania africana CBS 2517]
MP-----------------------GRF---------------TIIS-SSF-RRSIHKVPLRSHIQSVNAKSIIKINENQ
FNK-VSLYDYH--FFEELLPLEPVISYSLSKWLWFNYQLKHFPSFDLNIINVFTDLSQSVEMIHSIMKHFYTTLPRDLFQ
KINILLIPFYNCGHTKVTYQKVAVKNIPGNVQLLDNMSFCSIFDERPNTDNW--ESRLRSKLYMQEPTYFLLLNDIFKNS
SHDLLRYSKDTDSWKQCFVMENTQGQIH-KSFEQDIDFWCAKYIEIAFKENT---------------PNSGEVYIPTQLL
QFFHAMKVCFPDFKFLAIDTPQRWKPSLFNI-LKVS---------------TGQ---------MPIQTSKI-VQQMPNSY
GRCTFITEFMQLKAVCQKLNPG-------LIFEVQDLNEFVGDWIDYTKPNPY------------DTQSLHDPKQQVHLI
NKSSLAVLH-N
>XP_041407865.1 type II protein arginine methyltransferase [Kazachstania barnettii]
MNKLAM---------------GNKPKLH---------TF--IYRLNRGNSR-WQHTSSIPFRDRIELHNRKYIMKRH-NF
FSKHDSRYNGN--IQENLLTYDPILTQCIARWLWLNYKITDYPYYDLNILNIFTDLPQSIYFMKQIMKYYHETLPFESFD
KINYYLFPLYKCNNIN---KQSLLDDIPGNVHIMEDTTLFPI---NKNINFN--E--QTSNMYINDPVQILMFNDVLGKL
AHDLVRYNPYKQSLEQCYVEEN--GNINKKQYSSKLDYWCELTLRQLHNNDH-DHFSINENILGNNTYPMDEVSIPSQFI
QLLEQLKFNAPDLRLFMIDSPKIVTKPIIQK-LKRFFSRRKRYLYNDMIGASNI---------ENVESINV-VD---QIQ
SDITFNPDFQQLETILNNIKGNGTRHGFLQPCEIETLGNFCDKWVDSKVKEPSHSTN--KEDNSIPREFLEKLKLQLSIA
NKSSLTILH-S
>SMN22275.1 similar to Saccharomyces cerevisiae YKL162C Putative protein of unknown function [Kazachstania saulgeensis]
MNKVVM---------------GKRPRLQ---------TL--TYRLNSGQSR-WQHTDSMAFRDRIELHNRKYIMKRH-NF
FSKQDSISNGHGIPHENLLTYDPILTQCIARWLWLNYKITDYPYYDLNIFNIFTNLPQSIYFMKQIMQYFHEILPFESFD
KINYYLFPLYKCNHIN---KKSLLDNIPGNVHIMEDTTLFPI---NNNTNYI--E--QSNNMYINDPVQILMFNDILGKL
SHDMIRYNPKKQSLEQCYIEKN--GNIETKRYESQLDYWCELTLKQLYNNGY-DNIRK---------NQMNGVYIPTQFI
QLLEQLKFNAPDHRLFIIDSPKVVANPIIQR-LKNIFKRGQNFKSNDTMEWANK---------ANTNDPNISLD---RMQ
SYISFNPDFQQLETILNRVEGNDTRHGFLQPCEIETLGNFCDKWVDGKIKKPSLSSN-HEEEHSIPREVLDKLSLQLSIA
NKSSLNILH-S

  ```
</details> 
  
<details>
  <summary>Кластер # 6</summary>
    
  ```  
>SMN21413.1 similar to Saccharomyces cerevisiae YBR050C REG2 Regulatory subunit of the Glc7p type-1 protein phosphatase [Kazachstania saulgeensis]
MILFPSTCDNIRPNKYSDT--TNNDDDDLGPRVSMAVEAQNEEQFLRLSYKLKRTTSLRMGRKMQNGNS-----EESHQM
KQFLKESRQC--------RTFGLPSEENINVKDDVSIGQGTPDKYVDYLSYRWN--DFEVINSWKFIRLARKWCNERKNL
QMGTSSTTTTTTIEDKNLKPSELYNRRLENMSWRIWFKLKLSLTLQSNN-------SNNSNHDMTWLYGPLIHRDQSCSK
INIHTLNNKE-------NNQIPYIKPILKKRNLGETLEKNS-LWRLRKVKRNIKRRSSLDYRHIRQHTRLNIPTS---NP
YFVDDPLIESNDSSNFSSSSNSSSFTTLAAVTTTENSHKINNTDS-TTIINSPILND-DNDNDVRHIRFNNNVQQCIAIH
KSNSNLDLKQKKIKDIIQPLPSTQLNYYSGSESDSSSSDSNSCSDEECDNCKSNNNID-KHHNYIKNK--NKSKAVSHNV
NTSRRYPYIYDYNSVYTGDVSKFLPK-DYSCDIIDLPQGLGLELNVPQT-STGPSPIFETDLITTGDETLILSPT--ATT
PSISPLHSIIVASTAFSTPQTPLSSSAFGCSSTTSTLSTEGTETSSVQTMTKTRDFITGQLICNNSKNKINGTDQNKNSN
QILNAIETP--PTL-FNPKFKSSPTPLANFIFNSSDESD-----------------------------------------
------------------------------I
>KAG0655022.1 hypothetical protein C6P45_003206 [Kazachstania exigua]
MDNN------------------NCNKDDMGPSVSMAIYAKDNDQFLKESYNLRRTSSLKHSRKPQWHKC-DTVSSSTSSN
Q--------------------QYMTKDILTVKDDGSVPLQ-RTEYVDYLTYQWN--DFEIINSWKFIKLKK--CNS----
-------------------DNFLYNRRLENMSWRIYYRLKSQRC----N-------FVTKFDDFIWLYGPLIHRIKSASH
TTIIC-NNNN-------NPKPLKLKPILKKRNLRETLVKDS-LWKLKETKYKKQRS------------------------
-----------------NEGSNSSVNTLAVLSQ--CSL--NS-------------ND-QNESNSRHIRFNSNVQQCIATL
QDSH----------NNIKILPSVQLNYDDSDDSYSSDN------------DNNNNNID-YNDDEGHNPVIIKSYAVSHNV
TTRRRYPYIYDYNSVYTGDVTQFIPQ-DNTCDIIDLPQDIDLNLRMI-------------------------------TP
PENS----------PLSTPQSPISS-TFGNTSSISS----HTETSSIQ--TKTRDFITGQLISRPDENLLDN--------
------TPP--PIL-FNS-HKCA-ATFSKFIFNSSDESD-----------------------------------------
------------------------------L
>XP_041407085.1 uncharacterized protein KABA2_06S00946 [Kazachstania barnettii]
MLLIPSTYNNTTTTGDDDKKIDPREYEDLGPCVSMAIEAQNEEQFLRLSYKLKRTTSLHMGRKPGTAGA-ATGDAECRPT
KQFWKESRQC--------RTFALPSEETLRVKDDVSVGQGAPDKYVDYLSYRWN--DFEVINSWKFIRLARKWCHERKTL
QVDDG-------L-KDDLKPSELYNRRLENMSWRIWFKLKLPMALQPTQNVKEILFNSMSNQDMTWLYGPLIHRDQSGSV
ASIQNINDTKNI-----QKKTPYIKPILKKRNLGETLEKNS-LWRLRKVKRNIKRRSSLDYRHIRQHTRLNIPNTDRSAS
YFDDEPLIESNDSSNPSSSSTSSSFTGLAAITN-QHSHPHNDNDNNDSTTHSPILDDIQPQLDVRHIRFSNNVQQCIAIH
KSKSNLDSTEL-QKDIIQPLPPTQLNYYSGSESDSSSE---SCPDEDCDDCNKDTNVAYKHYSYIKNKSKSRSKAVSHNV
NTSRRYPYIYDYNSVYTGDVSNLLPK-DYSCDIIDLPQGLGLELSAPTQPIAIPSPTCETDILITSDETIILSPS--ATT
PSLSPSHSIIVPSSAFSTPQTPLSS-TFGYSSTTSTFSTEDTETSSVQALTKTRDFITGQLISSNSN-SANDDDSNKGSP
QLLDAMETP--PTL-FNPKFKTSPTALANFIFNSSDESD-----------------------------------------
------------------------------I
>XP_003956185.1 hypothetical protein KAFR_0C00550 [Kazachstania africana CBS 2517]
MMVSSNSY-----------------DMDL---------SEDTDR--YSSFKLKRTNSLNIVPSN----------------
----------------------------------------NSSISIDFETIKSNNDCWEILQSWKFIKSLQRLLIS-NNL
-------------------EIDIYSTRLENITWRTWCKVKPHFC-------------------RNWV-------------
-----------------RSTITTLKPILKKTSPSDSTVKNSQIWKSNKNKSFSNKE------------------------
--------------------------------------------------------N-FVHKKSKHIHFNNNVKQYIALT
SL------------TQLQLLPSTNLNDTGE-----------------------NNNTD-TPSN--------------YFT
NFKKGLNYNYDYNSVYTQDTSTFLPVLNCYTDIVDVPENINVSDL---------------------QKTISLSEE-----
-----------------------------------------IDTLSIT--THQ---------------------------
-----TQLP--PLL--KK--RSSSSNSSNFIFTSSSDSSS--------------------------SNSSLESLHKS---
-----------STF--------------SMF
>XP_022466418.1 hypothetical protein KNAG_0J00910 [Kazachstania naganishii CBS 8797]
MLEAGV----------------SSLQGDMGPSVSRAIEARDNVQFEKLSYCLKRTGHG-LTRCGGGGRSQDTL-VAYRQG
PRGVRARRRSRRRLSYDESAGGLLPADLLAMKDDNDLSIVVPGKYVDYLNYNWRGDVRELWNSWKFLAMWKRMVSG--KF
--------------RGD-IPDLVTIGRLENIIWRIWLLLVRSRRSGGNAGAARKHEVVLPEGDVPWLYGPIVTSDYSSVD
VTARETTAESATAAPTATGTDDTLKPILKKTALGEQIVENS-IWKLKQMHQWKQE------------VKSNVIDS-----
-----------------------EKSILQDVT------------------------S-TDGAPSRHITFDTTVHQYIALS
NSISPFH-------SSIRLLPDTHLNYSSDEDSDGNGD-----GTESGDGAENGDGTE-QHW---QGGTAATRNAVSHN-
-TSRSHTYFYDYNSVYTNDVSSLIPCTDPHTDVLDVPENLNLLGL---------------------SETLVRPLEVDATP
PVAAPLSP-RVDGSEQQPPASPLP-------------------------VTKTRDFITGEFLQ-----------------
----AAETPATPVLHPQPAFKHS-VSSSTFVLTSDDEENALMDEPIPREDDDLVYARMLGQRSLSTSNYTTTSVEESNGN
LSEIDYEEEPGSEFSTKIGLARQWDPSTLNG

  ```
</details> 
  
<details>
  <summary>Кластер # 7</summary>
    
  ```  
>KAG0663124.1 ornithine aminotransferase [Kazachstania exigua]
-----MSKEAIYLEEKYSAHNYHPLPVVFDHALGAKVWDPEGNEYLDFLSAYSAVNQGHCHPAIIKALVDQAHKVTLSSR
AFYSEAFAHFAQYITEYFNYECVLPMNTGAEAVETSLKLARRWGYMVKKIPENEAIILAASGNFHGRTFGAISLSTDEQD
SRAQFGPFLENTHAGEPLG-STIRYGHAEDLQKILEKHGDKIAAIILEPIQGEAGIVVPPPEYFPRVAELCREYNVLLIC
DEIQTGIGRTGKLLCSEHY-GIKPDIVLLGKALGGGVLPISAVLSSRAIMDCFTPGSHGSTFGGNPLACAVSMAALAVVR
DEKLVDRAAELGGYFLEQLNKLKAESQGMITEVRGVGLLTAIVIDPSRTPANKTAWDLCLLMRDNGVLAKPTHDHIIRLA
PPLVISKEDLDKGIDAIRHSLSTL----
>XP_003957699.1 hypothetical protein KAFR_0E04130 [Kazachstania africana CBS 2517]
MEFTLSSEDTFKYESKYSAHNYHPLPVVFHKAQGAHVWDPEGREYLDFLSAYSAVNQGHCHPKIIRALIDQATELTLSSR
AFSNDVFAQFAKYITEYFEYEMVLPMNTGAEAVETALKLARRWGYQVKGIPENEAIILGAQGNFHGRTFGAISLSTDFED
SKKDFGPFLANTSSCLPGTKKEIRYGVIEDLEEALSMYGEKICAIILEPIQGEAGIVVPPMDYFPKVSALCKKYNVLFIC
DEIQTGIGRTGKLLCCDHY-NVKPDIITLGKALSGGVLPVSCVLSSRDIMLCFSPGSHGSTFGGNPLASRVAIAALQVIK
DENLVERAAKLGQILQNELWKLKEVSGGVISEVRGMGLLTAVVIDPTKTG-GKTAWDLCLVMKDFGVLAKPTHDHIIRLA
PPLVISEDDLKKGIQAIAKSLQKLKENA
>XP_022463313.1 hypothetical protein KNAG_0B06390 [Kazachstania naganishii CBS 8797]
M---LSSEQTIEWEQKYSAHNYHPLPVVFHKASGAHVWDPEGREYLDFLSAYSAVNQGHCHPKIVGALVEQAQLLTLSSR
AFHSDAFAEFAKYVTEYFQYDMVLPMNTGAEAVETALKLARRWGYEVKGIPENEAMVLGAQGNFHGRTFGAISLSTDAED
SRKNFGPFLANTSAVSPHSNAPIRYGVIEDLQLAFEHQGGKLAAVILEPIQGEAGIVVPPEGYLSQVQQLCRKHNVLFIC
DEIQTGIGRTGKLLCSEHSPGVKPDIVLLGKALSGGVVPCSAVLASREIMLCFAPGSHGSTFGGNPLASKVAVAALQVIK
DEKLVERAAELGELLLGELRRLQELSGGVIAEVRGVGLLTAIVIDQTRTK-GKTAWDLCLAMREHGVLAKPTHDNIIRLA
PPLVISKEDLLRGCKAIEAALNTL----
>XP_041408366.1 ornithine-oxo-acid transaminase [Kazachstania barnettii]
-----MSEEAILMEEKYSAHNYHPLPVVFDHALGAHVWDPEGKDYLDFLSAYSAVNQGHCHPTIINALVKQAHKLTLSSR
AFYSEAFAEFAKFITEYFDYECVLPMNTGAEAVETALKLARRWGYMVKKIPVGEAVILAAQGNFHGRTFGAISLSTDEQD
SRLHFGPFLKHTHAGGPLG-TTIRYGVAEDLEKVLAAHGKTVAAVILEPIQGEAGIVVPPADYFPRVTELCRQHNVLLIC
DEIQTGIGRTGQLLCSQHY-GIKPDIVLLGKALGGGVLPVSAVLSSRAIMDCFTPGSHGSTFGGNPLASKVAIAALQVVR
DEKLVDRARDMGGYFLDQLRQLQKESGGTISEVRGVGLLTAIVIDPARTG-GHTAWDVCLAMRDNGVLAKPTHDHIIRLA
PPLVISKEDLDKGIEAIRKALKSF---N
>SMN21966.1 similar to Saccharomyces cerevisiae YLR438W CAR2 L-ornithine transaminase (OTAse) [Kazachstania saulgeensis]
-----MSEEAIRLEETYSAHNYHPLPVVFDHALGAHVWDPEGKEYLDFLSAYSAVNQGHCHPDIIKALIEQSQKVTLSSR
AFYSEAFAQYAQFITEYFNYECVLPMNTGAEAVETALKLARRWGYMTKKIPKGEAVVLAAQGNFHGRTFGAISLSTDEQD
SRLHFGPFLKHTHSGGPLG-TTIRYGVAEDLEKVLHKHGSTIAAIILEPIQGEAGIVVPPADYFPRVSKLCQQYNVLLIC
DEIQTGIGRTGKLLCCEHY-GIKPDIVLLGKALGGGVLPVSAVLSSRSIMDCFTPGSHGSTFGGNPLASKVAIAALKVIR
DENLVDRSKELGGYFLDQLRVLQKESQGIISEVRGMGLLTAIVIDPSRTN-GHTAWDVCLKMRDFGVLAKPTHDHIIRLA
PPLVISKEDLDKGIDAIRNALATF----

  ```
</details> 
  
<details>
  <summary>Кластер # 8</summary>
    
  ```  
>SMN21125.1 similar to Saccharomyces cerevisiae YDR101C ARX1 Shuttling pre-60S factor [Kazachstania saulgeensis]
MELAVSHEDSQILLKDKNVLQDSVVDKYRTAGQITQTALKYITGLINDIYHYRTIENPLTISELCLLTDSFIVTRLEQYY
KNKVNERGIAIPTSIDVDQLAGGWSPEIDDIKNLKNWNKETTSV-EDPLNSTVTGILKAGDVVKITLGVHIDGYTSEVSH
SMVIYPTSTNEAGVVVPTGPLLDVKADAVAAAHIAIETVVALLSCALTPEKLPATLGTSVTGQLIRHVVNTIARSYNCAI
VPGSRVRRIRRFLAGQNEGIVAEREYKGVVWTESHQEAELLANSEVKDLTVATNSSRSAPSAIPVDDFVVKAGEVYLVDL
KMVPLGQTTKKGLVTLEVVDSAKGKSHRKNELVARSGIFVRDFAQSHALKLKTSRKLLTNIDRNGVYPFKLSHLSENFPI
ISTKDYNEQIVALDKDLKSFRLGMSEIINNYLCVETPIEVAKWVPWDHILKVSNQNGALSYDATASLTLPGHEVPLPKLG
IATLKLKSLVRSSSETIDLPVVRECTTVVLCDSDTSSGERPELLRLTGGSKTTQPSWIQSKLELNNEDPTVQGIFQLATL
VKDKRFGLIVRETQPMKQSVNQGSNENKDMEL
>XP_022465966.1 hypothetical protein KNAG_0H03060 [Kazachstania naganishii CBS 8797]
MDLAVSHEDTEILLKDKNVLQESVLDKYRTAGQISQTALKYVTGLINDMYHFKNTDRQLRIEELCLLTDSFMMTRLEQYY
KHKVNERGIAIPTTIDVNQIESSWCPEIDDIANLEKWNKDQITREDAPYHSVVQGLLKEGDVVKITLGVHIDGYTSEVSH
TMVIYPVDNSIDGQPKPAGPLLGGKADAVAATYIAMEAVVSLLACSLTPEKLPASFGSAVNGYAIRSIVDTIARSYNCAV
VPGSRVRRIRRFLAGQNEGIVAEREYKGVIWTESHEEAKLLANTEVKDIAVSQPSVPRVVSAVPTDDFVVKAGETYLIDL
KFAPLENLDKKGLVILETVDAYTGKSHRQNQLIARSGAYLRDYAQSHTLKLKTSRQLLTKIDNNGVYPFKLSHLSSAFPI
SKEGNLDDQLAAISGDLKSFRLGMSEISNNYLCVEKPIQVAQWVPWEHILKSNNPNGNLSYDASAALTLPGHDLPLPKLG
MSALKLKAVAKSTRETVELPVIRECSTVILCADDVGVNGRPEVLRATGGSKTCATSWVHSVHEMNKEDPIVQGIFQLGVL
SQDKRFGLNIRETQPMKHRVDTP--VNDAMEL
>XP_003955962.1 hypothetical protein KAFR_0B05320 [Kazachstania africana CBS 2517]
MELAVSHEDSQILLKDKNVLQESVLDKYRTAGQIVQTALKYITGLINDAYHYKTIERPLTISELCLLADSFMVTRLDQYY
KNKVNERGIAIPTTIDVDQISSGWAPEIDDDVNIKNWNKGTTSQ-ADPFGSVVTGFFKEGDIVKISLGVHIDGYTSQASH
TMVIYPVDASTSAAPKPAGPLLGGKADAIAATHIATESVNALLSCALTPEKLPPSLGTKVNGQLIRLVVDTIVRSYNCAV
VPGSRVRRIRRFLAGQNEGIVAEKEYKGVIWTESHQEAHLLSNTDARDLSVVKGSNNNVLSAVPTDDFTVEAGEAYLVDL
KVCPLDQFNKKGLVTLQTIDSYTGKSHKETELVARSGMYIRDYAQSHQLKLKTSRQLLTKIDRQGVYPFKLAHLAQSFPV
KSEEGFDEQIQSIKKDLKSFRLGMSEISNNYLCVESPIQVAKWVPWDHIIKATNPNGNLSYDATAALTLPGHEVPLPKLG
VSALRLKSLMKSSKETVEVPVIHECNTVVLCGTEVSLSDRPELLKVTGGSKTCQPSWVHSKHELNQQDSVVQGVFKLAAL
AKDKRFGLLMRETQPMKQSAQ-----------
>XP_041407562.1 putative hydrolase [Kazachstania barnettii]
MELAVSHEDSQILLKDKNILQDSVVDKYRTAGQITQTALKYVTGLINDIYHYRTIETPLTISELCLLTDSFIVTRLEQYY
KNKVNERGIAIPTSIDVDQLAGGWSPEIDDIKNLKNWNKETTSE-EDPLNSTVTGLLKPGDIVKITLGVHIDGYTSEVSH
SMVIYPTSTNEAGIVVPTGPLLDIKADAVAASHIAVETVIALLACALTPEKLPATLGTSVTGQLIRHVVNTIARSYNCAI
VPGSRVRRIRRFLAGQNEGIVAEREYKGVVWAESHQEAELLANSEVKDLTVATNSSRSAPSAIPVDDFVVKAGEVYLVDL
KMVPLGKTTKKGLVTLEVVDSAKGKSHRKNELVARSGIFVRDFAQIHALKLKTSRKLVTKIDRNGVYPFKLSHLSENFPI
ISSKDYNEQISALDKDLKSFRLGMSEIINNYLCVESPVEVAKWVPWDHILKVSNQNGALSYDATASLTLPGHEVPLPKLG
IATLKLKSLVRSSSETIELPVVRECTTVVLCDSDISSGERPEVLRLTGGSKTTQPSWIQSKLELNNQDPTVQGIFQLATL
VKDKRFGLIIRETQPMKQNIGQSSNENKDMEL
>KAG0661944.1 putative metalloprotease arx1 [Kazachstania exigua]
MELAVSYEDSQVLLKDKNVLQDSVVDKYRTAGQISQTALKYVTGLINDIYHYKTIETPLTISEICLLADSFIITRLEQYY
KNKVNERGIAIPTSIDVDQLASGWSPEIDDVKNLKNWNKEITSE-EDPLNSSVTGLLKVGDVVKITLGVHIDGYTSEVSH
TMVIYPTSTNETGAIVPAGPLLDVKADAIAANHIAMETVVALLACALTPEKLPASLGTAVTGQLIRHIVNTVARSYNCAV
VPGSRVRRIRRFLAGQNEGIVAEREYKGVVWTESHQEAELLANSDVKDLAVATNSSRSVPSAIPVDDFTVNSGEVYMIDL
KMVPVGHSTKKGLVTLDVVDSAQGKSHRKNELVARSGIFVRDFAQSHALKLKTSRKLLTNIDRNGVYPFKLSHLSENFPI
VQDKDYNEQIAALDKDLKSFRLGMSEILNNYLCVESPIEVAKWVPWEHILKGSNQNGALSYDATATLTLPGHEVPLPKLG
IASLKLKSLMKSCPETIDLPVVRECTTVVLCDSDVSSGDKPELLRLTGGSKTSQPSWIQSKLELNSEDSTVQGIFQLATL
VKDKRFGLVIRETQPMKQVVNQGSKENNGMEL

  ```
</details> 
  
<details>
  <summary>Кластер # 9</summary>
    
  ```  
>KAG0668030.1 hypothetical protein C6P45_005120 [Kazachstania exigua]
-----------METLNEQQLQAVQFDPTAALQVVAGPGTGKTKVLVARVANLIINYHIQPQNIIVTTFTNKAATEMKQRL
AQLLSNTQVNINDLIIGTFHSVCLRILSKHGHLISLNPGWKIIDEKETDKIINDIIMAIPDQIRDYATSFKRIINLCRPS
-KKGDGWSIHPKLVKREISRLKSLALLPDEYLKQSTHDEALAYCYTQYQLQLHSLNSLDFDDLLMFTFRLLCSHRCLPHI
QHVLVDEFQDTNSIQMDLMFLLAKGNHHISRGITVVGDPDQSIYAFRNALAHNFQEMNNKCPLPCSQVVLIQNYRSSQRI
LDTSETLIKQQVRGRQERLPLRAQFNCDFPPVYINFPVSFIQGPSLAKEILYLKALPNLFNFDHFAILVRQRRQIKSIET
ALIEHRIPYKIVKGHAFWELKEITSMLNYLNCLYTDTDYNAIVASLLYPARGIGQTSATKILSLFKDHE--SSSSPWKIL
EEISSGKHALGINAKGKNVITIFIQMIQKCQSLMKANTADKETLTQIFNTLYKMSGMEKEYIYMDGKEQL----------
-TEPNLENPRHKNIQILRNFFLEERELESLPSNPN-ILTPP--ET-TT---QSP-IKNHMRNFFNSLSLFTSSDKISSS-
------QRDSDLPEGAVTISTIHGSKGLEWPVVFIPGCVEGIIPSIFQSDNKD--------DSESDS--ESDS-KS----
--SQNTKKPTNMDENLDEERRMFFVAQTRAKYLLYLSSVETSNNPMFGGPSRFFTPEVMKTLTDDQKALESVHNIKELYK
AMDVK-PIKNNPDFSFNTLVKDYSKFLENRRESMIWSGNVVRNTNTLDLSR-NKISLANPISSFTTAAAIALESGQTYQ-
--KQYAPTYSPTRR--NLGSGPQGQLSPVKKHAPRLNIKGSPS--------------PTRNFAPTARNP---ESPTKKFA
PLK-LRNNIQVPPMYA---------TPSPRLERSPKPMSFDNKVPDR-----------------VS-NIQ----------
ARRNVRRITSTPIQLSD-MK-V---NPVKSEFP-KSPKLEDTTAAEILHNPADMIVDNRPIISNAKTLANAIRKNPIAKV
-TTKKKKA---------TTNTAVKKETKIEPATLE----NRKPLKNENDKTLKTTQAKKK--------KVKKEPCSSQVD
IFSQLARAKKKAKIDNNEIIILDD
>XP_022462870.1 hypothetical protein KNAG_0B01810 [Kazachstania naganishii CBS 8797]
MQQCDNDLDRILSSLNKQQRLATEFDPTQVLQIIAGPGTGKTKVLTSRVAFLLLKHKWSPKDIVVTTFTNKAAKEMVERL
TSMLAHTGVNVGDLNIGTFHSVCLRILTRFGDKIGLTPGWRIIEEKEVDAIVNEMIEKTPDQVRDYASSFDRIVNLCRPK
-GNGEEWVIHPKMIKKEISRLKSCAILPEEYANESVHDSALAHYYEVYHKELTKLNALDFDDLLMYCFRLLSEERCMPHI
KHVFVDEFQDTNSIQMDLMFMLAKGNHHVSRGITVVGDPDQSIYAFRNALVHNFQEMANKSPLQCSQIVLIENYRSSQKI
LNTSETLIKQQTKGRTLRTPLHAQFDCKFPPVYVNFPVQFLQGTSLAKEILYLKALPSLFSYSDFAILVRQRRQIKSIES
ALIEHRIPYHIIRGRAFWDLKEITAILNLLRCVYSDNEKNALLTSLLYPSRGLGQTSADKLTLLMDQN---PLESPYNVL
KNVASNQLPFSGGNKIKSVIISFVHMIDSCRSLLGQ--PPSTVLEGIFDQLYQMSGLQQEYLYVDGKNKSSDTGSERDIT
AKAPNYENPRHKNVMLLKSYFMENKAIEDLLIDQK-NETSNGVSNSGSDGKELD-AKTYICNFFNSLSVFTTELSETDTL
AD----DDKNKNGEGQITISTIHGAKGLEWPVVLIPGCVEGIIPSIFSKDDEDEDIDEDDEDNDAEQSNENKTSKN----
--NTNSKRGKNTEATLDEERRMFFVAQTRAKVLLYLSSVTESNNATVGGPSRFLTPELMSTMVDDQKVFQNEQNIKALYK
ALGKG-MPSLEPSFSIKQLVRDYSKFIQNSR-IFVWNGDGVRKSATPGFTEQHQAPMAALNAEFTTAAA-QLKVESPEKN
PVKMYS-AMSSSKR--SSVKG-KDFSSSAKSYAPTSIRKVAHRPSIKAPDNYGKVATKRKLFVSPTNSPAKTENNTKKSC
LNH-IPDSNLS-PQIT---------TPRVNLEQADTHSNYFNQ---------------------GS-QTT----------
RRPSSRKINTQPIKIGTHAS-ITEHEPIY-EVKPEPSRWEDTTAAEILHNPDDLTVDNRPIFATAKTLAKAVKK-PT---
--------------------------------------------------------------------------------
------RTKVKKNLERISQILVTK
>XP_003954718.1 hypothetical protein KAFR_0A01450 [Kazachstania africana CBS 2517]
MAMPNTVLGQLLATLNKQQRIAVEFDPNNALQVIAGPGTGKTKVLTSRVVYLLLHHKIEPKDIVVTTFTNKAAKEMMDRL
AKMLSGTAIRVDEITIGTFHSICLRVLLKYGFKVGLNRGWRIVEEKEVEAIIHDLIKTMPDQIRDYANSYKRSVNLCRPT
-RNKDEWAVHPQMVKKEISRLKSNALLPEEYENDSNHDPALAHFYTKYQSELGKLNALDFDDLLMYTFRLLTKERCLPDI
KHVLVDEFQDTNSIQMDLMFLFAKGDHHVSRGITVVGDPDQSIYAFRNALAQNFQQMQQKTPLHCSQVVLVENYRSSQKI
LDTSETLIQQQIKGRTHRAPLRAQFDVEFPPVYVNFPVGFLQSASIAREILYLKALPNLFSYNDFSILVRQRRQIKNIET
ALIEHRIPYKIVKGRAFWELKEISAMMHLIKCAYSDNEKFSILSSLLYPAKGLGQTSADKIKKIFEDN---PSQTPFSLL
QDIEKGAINLTMTTKVRSVIKDFIQMINFSRSFDKA--PLKSSLENIFDTLYERSGMKNEYLYFDGGKKSDT----N-DS
NREANYENPRHKNILLLKKYFLGIDEIEDFIHSQSDQKTFI-EDIQQV---DTNVIRSYIRTFFNSLSLYATESTSSDNE
IDRTSKRKNSRNGEACVTISTIHGAKGLEWPVVFIPGCIEGIIPSIFSRDESSS-------ETESDT--EEEG-TNTSDK
NVPKSNKKSSSLEEPVDEERRMFFVAQTRAKLLLYLSSIKEGENPTQGGPSRFLTPEVRKTLINEQNALKNEKNIELLYK
SMNKKVPSDLIKRFSLKKLVQDYAQFIENRRESMIWNGRVIRNSFTLDITR-NTVAMDDPISDFTTAAA-HLQTEVNKK-
--PVLERQFQTMSRKGSTLSS-TSKLWPKKAYAPQANQRLSPS--------------PPKVHAPTTTYPLQ-ESPTKKKS
YAPSYPHKPYS-TTGTEFKIKQNKTDNDNILEKPFPISASNDRASNPKMLATSKGSTNEAIKKELFSQNQVISSPKRISR
TKSVTRKLIVSPIMIED-KKRY---EEVKKNGSVHHTVAGDRTAAEILHDPDDLIIDNRPILTSAKTLMKAIKK-ADSKS
NQSSQKSF---------------------------------------SEHQLK-----------------TEEASSSQFD
ILSQLSRAKKKAKLNDGEIIVIDD
>XP_041408799.1 DNA helicase SRS2 [Kazachstania barnettii]
-----------MDTLNEQQRQAVQFDPSAALQVVAGPGTGKTKVLVARVAHLILHYNIPPQNIVVTTFTNKAAMEMKQRL
QDLLQNHDVPLNDLIIGTFHSVCLRILMRYGGLIGLTSGWHILDDKEVDKIILETIQQMPDQIRDYATSFKRSINLCRPS
KKNGDGWAVHPKIVKREISRLKSMALLPEEYIQQSTHDEALAYCYSTYQSQMNSLNGLDFDDLLMFTFRLLCKHRCLPQI
QHVLVDEFQDTNSIQMDLMFLLAKGNHHLSRGITVVGDPDQSIYAFRNALAYNFQQMANKCPLPCSQVILVENYRSSQRI
LDTSETLINQQQHGRQQRLPLKAQFDCDFPPVYTNFPVSFIQGPSLAKELLYLKALPNLFTYDSFAILVRQRRQIKSIET
ALIEHRIPYKIVKGHAFWELKEITSMLNLLNCLYSDNNPNAIISALTYPARGLGQTSASKITSLMKEQQMKESMSAMDTL
REISTGKHNLGMNSRAKYVITKFISMIQSCRDTFYSTTTKTTALTEIFDTLYKMSDMENEYLSQDGKENRNNKEIDK-TS
NTDPNLDNPRHKNIQLLKKYFLETKEVEELPNDAK-MSVPI--DDMKH---DSP-IVEHIRTFFNSLSLFTADSVSENN-
------GQSSRLKEGAVTISTIHGSKGLEWPVVFIPGCIEGIIPSVFQSDNKE--------DSDSESSTENDA-SN----
--DKNPKLPTNADESLDEERRMFFVAQTRAKYLLYLSSVEESNSPMFGGPSRFFTPEVMKTLTDQQMALDSLSNINKLYR
AINVR-PEKLNQDFSFNTLVKDYSKFVENRRESMIWAGNVLRNMASLDLSR-NKLPAPNAISSFTTAAA-ALKIETNNK-
--KQYAPSYSTTKR--TLGEQ-SLQLSPGRKCAPTNNVRRSPS--------------PQRQFAPCTRAP---ESPTKKFA
PPPQLNNNIGI-TLSA---------NSTSKLDSSFSRPSPDERVSER-----------------VG--AQ----------
FRRSARRITSTPIQLTE-TS-I---NSVNNEISIPKTKLEDTTASEILHNPDDLTVDNRPIFSNARTLANAIRN-PKSKG
KESKKKKVTVKKEPSKKTTFTKTKKSAKKEPAKASSSTNIKLALKKETNNDLSSTKNKKRVQTAGPISNVKREPSSTQVD
IFSQLANARKKAKIEKSEIIILDD
>SMN21722.1 similar to Saccharomyces cerevisiae YJL092W SRS2 DNA helicase and DNA-dependent ATPase involved in DNA repair [Kazachstania saulgeensis]
-----------MDTLNAQQKQAVQFDPSAALQVVAGPGTGKTKVLVARVAHLILHYNIPPQNIVVTTFTNKAAMEMKQRL
SVLLKDQDVSLNDLIIGTFHSVCLRILMRFGGMIGLPSDWRILDDKETDKIVMDTIQQMPDQIRDYATSFKRTINLCRPS
KKNGDNWVVHPKIVKREISRLKSSALLPEEYIQQSTHDEALAYCYSNYQTQMNALNGLDFDDLLMYTFRLLCKHRCLPQI
QHVLVDEFQDTNSIQMDLMFLLAKGNHHLSRGITVVGDPDQSIYAFRNALAYNFQQMANKCPLPCSQVILVENYRSSQRI
LDTSETLINQQQHGRQQRLPLRAQFDCDFPPVYTNFPVSFIQGPSLAKELLYLKALPNLFTYDSFAILVRQRRQIKSIET
ALIEHRIPYKIVKGHAFWELKEITSMLNLLNCIYSDNDSNAIVSALTYPARGFGQTSASKMLSLMKDKQVNESMSAMETL
REVSAGKHNLGMNAKAKSVINKFINMIQSCREKFQNTSSMATTLSEIFDSLYKMSDMENEYLTQDGKENRNNKENSA-NS
NKDANLDNPRHKNIQLLKNYFLETKEVEQLPTDTQ-YSLPR--DDSQK---DSP-IIEHIRTFFNSLSLFTADNISDSD-
------KQDSRLKEGAVTISTIHGSKGLEWPVVFIPGCIEGIIPSIFQSDNKE--------DSDSDSSTGGDT-SN----
--DKNSKRPTNADESLDEERRMFFVAQTRAKYLLYLSSVEESNSPMFGGPSRFFTPEVMKTLTDEQKALDSISNINKLYR
AISAK-PEKLNENFSFHTLVKDYSKFVENRRESMIWGGNVLRNLASLDLSR-NKLSMATPMSSFTTAAA-ALKIETNNK-
--KQYAPSYSPTRR--TQGER-SLQLSPIRKCAPTNNINRSPS--------------PKRQFAPPTRAP---ESPTKRFA
PPPQWNNNVRN-PSAT---------GQTSLLESSFSKSSLEERVSDR-----------------AG--SQ----------
FRRNARRITSTPIQLSE-VT-V---SPINNEVPPPRSKFEDTTAAEILHNPDDLTVDNRPIISNARNLANAIRN-PISKE
KTTKKKKAAVKKEPSKNSASLKCKTSVKKEPIK------VKPTVKKESENDLKSTKSRKRVKVVDPSSRVKKEVSSTQVD
IFSQLANAKKKAKIDKSEIIILDD

  ```
</details> 
  
<details>
  <summary>Кластер # 10</summary>
    
  ```  
>KAG0667900.1 pre-rRNA-processing protein pno1 [Kazachstania exigua]
MVAPTALKKSDIPEAF----STSGASRIVGLNNTEMIDDE-EDEDILIDQEDETNRT-EQEGND-EEITKKKETKGVVFD
ESGKPRFASANKTTLTKIKLESRKIAVPPHRMTPLRNSWTKIYPPLVDHLKLQVRMNLKTKSVELRTNPKFTKDPGALQK
GADFIKAFTLGFDLDDAIALLRLDDLYIETFEVKDVKTLNGDHLSRAIGRIAGKDGKTKFAIENATRTRIVLADSKIHIL
GGFTHIRMAREAVVSLILGSPPGKVYGNLRTVASRLKERY
>XP_022463809.1 hypothetical protein KNAG_0C04610 [Kazachstania naganishii CBS 8797]
MVAPTAIKSNADSA--GV-SAPITASRIVGTDNTQPIENEDDDEDVLLDSGMAVDEDGEGKGSDNGAANTKREHKGVVLD
EQGKPRFSSANKASETKIKAESRKVAVPPHRMTPLRNNWTKIYPPLVDHLKLQVRMNLKTKSVELRTHPKHTTDPGALQK
GADFIKAFTLGFDLDDSIALLRLDDLYIETFEVKDVKTLHGDHLSRAIGRIAGKDGKTKFAIENATRTRIVLADSKIHIL
GGFTHIRMARESVVSLILGSPPGKVYGNLRTVASRLKERY
>XP_041405574.1 Pno1p [Kazachstania barnettii]
MVAPTALKKTTVPETGNN-AASISSSRIIGMDNTEMIED---DEDILIDQDDNVAVS-TENGPT-EEIKKQKESKGVVFD
ESGKPRFAQANKTTLTKIKLESRKIAVPPHRMTPLRNNWTKIYPPLVEHLKLQVRMNLKTKSVELRTNPKFTTDPGALQK
GADFIKAFTLGFDLDDAIALLRLDDLYIETFEVKDVKTLNGDHLSRAIGRIAGKDGKTKFAIENATRTRIVLADSKIHIL
GGFTHIRMARESVVSLILGSPPGKVYGNLRTVASRLKERY
>XP_003957646.1 hypothetical protein KAFR_0E03600 [Kazachstania africana CBS 2517]
MVAPTALKSSA-SETFSPTSSGPVPSRIIGTNNNQTLEDE-DDDDILLDQENAGEDA-SLEQNG-EESKKKKESKGVVLD
EEGKPRFSSAKKSNETKVKLESRKVPVPPHRMTPLRNNWTKIYPPLVEHLKLQVRMNLKTKSVELRTHPKHTTDPGALQK
GADFIKAFTLGFDLDDSIALLRLDDLYIETFEVKDVKTLTGDHLSRAIGRIAGKDGKTKFAIENATRTRIVLADSKIHIL
GGFTHIRMAREAVVSLILGSPPGKVYGNLRTVASRLKERY
>SMN19646.1 similar to Saccharomyces cerevisiae YOR145C PNO1 Essential nucleolar protein required for pre-18S rRNA processing [Kazachstania saulgeensis]
MVAPTALKKTAVSEVSNVASSATTSSRIIGMDNREKIEDD-EDEDILIDQDDADDVT--PTQND-EEIKKQKESKGVVFD
ESGKPRFAQANKTTLTKIKLESRKIAVPPHRMTPLRNNWTKIYPPLVEHLKLQVRMNLKTRSVELRTNPKFTTDPGALQK
GADFIKAFTLGFDLDDAIALLRLDDLYIETFEVKDVKTLNGDHLSRAIGRIAGKDGKTKFAIENATRTRIVLADSKIHIL
GGFTHIRMAREAVVSLILGSPPGKVYGNLRTVASRLKERY

  ```
</details> 
  
Визуализация расположение Z-ДНК для кластеров
---
![image](https://user-images.githubusercontent.com/23341597/173206932-656adae3-5af6-4b4c-80f8-93d1f554772a.png)  
![image](https://user-images.githubusercontent.com/23341597/173206940-12029138-b0b8-47f7-b43f-8258a97b110d.png)  
![image](https://user-images.githubusercontent.com/23341597/173206951-dd21f741-128c-45f0-a095-f352714ea923.png)  
![image](https://user-images.githubusercontent.com/23341597/173206961-4e34a803-6f55-44db-afd1-cee3e26ba787.png)  
![image](https://user-images.githubusercontent.com/23341597/173206967-9e94b5be-d6cc-47e3-93b7-898d7fd9b64c.png)  
![image](https://user-images.githubusercontent.com/23341597/173206975-1b9acde9-20eb-4dd4-8c1d-da698b70e8a4.png)  
![image](https://user-images.githubusercontent.com/23341597/173206995-046808a9-cce2-4698-9677-4c40711786b1.png)  
![image](https://user-images.githubusercontent.com/23341597/173207006-5c9807f3-4c79-4696-9384-d4491105aa3a.png)  
![image](https://user-images.githubusercontent.com/23341597/173207012-33ebd122-bdeb-47a3-a7fc-757320e2956b.png)  
![image](https://user-images.githubusercontent.com/23341597/173207021-cf5d229f-239d-4ad5-9952-ac8b432f8515.png)
  
  
