# AVALIAÇÃO ENTRE SPRING-MVC VS SPRING-WEBFLUX
Este projeto tem como objetivo comparar o desempenho de duas tecnologias Spring MVC e Spring WebFlux. 
Foram realizados testes de carga utilizando o software de teste de carga "k6".

Os testes foram executados com 500 e 1000 usuários virtuais (VUs), com duração de 10 segundos. Os resultados foram coletados e apresentados abaixo.

Resultados
## Spring MVC - 500 VUs - 10s
default ↓ [ 100% ] 500 VUs  10s                                         

     ✓ status is 200

     checks.........................: 100.00% ✓ 1250      ✗ 0
     data_received..................: 158 kB  11 kB/s
     data_sent......................: 120 kB  8.3 kB/s
     http_req_blocked...............: avg=83.78ms  min=970ns   med=3.84µs  max=366.33ms p(90)=280ms    p(95)=305.08ms
     http_req_connecting............: avg=58.03ms  min=0s      med=0s      max=305.39ms p(90)=167.04ms p(95)=201.88ms
     http_req_duration..............: avg=3.78s    min=1.29s   med=3.79s   max=8.92s    p(90)=5.12s    p(95)=5.95s
       { expected_response:true }...: avg=3.78s    min=1.29s   med=3.79s   max=8.92s    p(90)=5.12s    p(95)=5.95s
     http_req_failed................: 0.00%   ✓ 0         ✗ 1250
     http_req_receiving.............: avg=386.38µs min=10.45µs med=76.88µs max=10.22ms  p(90)=832.99µs p(95)=1.79ms
     http_req_sending...............: avg=244.63µs min=4.71µs  med=15.28µs max=9.11ms   p(90)=444.15µs p(95)=1.77ms
     http_req_tls_handshaking.......: avg=0s       min=0s      med=0s      max=0s       p(90)=0s       p(95)=0s
     http_req_waiting...............: avg=3.78s    min=1.29s   med=3.79s   max=8.92s    p(90)=5.12s    p(95)=5.95s
     http_reqs......................: 1250    86.277611/s
     iteration_duration.............: avg=4.86s    min=2.44s   med=4.79s   max=10.13s   p(90)=6.38s    p(95)=7.15s
     iterations.....................: 1250    86.277611/s
     vus............................: 66      min=66      max=500
     vus_max........................: 500     min=500     max=500


running (14.5s), 000/500 VUs, 1250 complete and 0 interrupted iterations
default ✓ [ 100% ] 500 VUs  10s

## SpringMvc - 1000vus - 10s
-------------------------------------------------------------------------------------------------------------------------------

running (17.8s), 0021/1000 VUs, 2066 complete and 0 interrupted iterations
default ↓ [ 100% ] 1000 VUs  10s

     ✓ status is 200

     checks.........................: 100.00% ✓ 2087       ✗ 0
     data_received..................: 263 kB  14 kB/s
     data_sent......................: 200 kB  11 kB/s
     http_req_blocked...............: avg=187.56ms min=940ns    med=12.43µs max=617.44ms p(90)=523.06ms p(95)=549.11ms
     http_req_connecting............: avg=112.3ms  min=0s       med=0s      max=536.89ms p(90)=310.89ms p(95)=353.46ms
     http_req_duration..............: avg=5.55s    min=217.56ms med=6.87s   max=10.08s   p(90)=7.9s     p(95)=8.01s
       { expected_response:true }...: avg=5.55s    min=217.56ms med=6.87s   max=10.08s   p(90)=7.9s     p(95)=8.01s
     http_req_failed................: 0.00%   ✓ 0          ✗ 2087
     http_req_receiving.............: avg=1.53ms   min=11.35µs  med=52.2µs  max=110.97ms p(90)=867.7µs  p(95)=3.82ms
     http_req_sending...............: avg=406.74µs min=4.36µs   med=20.02µs max=182.48ms p(90)=201.72µs p(95)=691.25µs
     http_req_tls_handshaking.......: avg=0s       min=0s       med=0s      max=0s       p(90)=0s       p(95)=0s
     http_req_waiting...............: avg=5.55s    min=217.47ms med=6.87s   max=10.07s   p(90)=7.9s     p(95)=8.01s
     http_reqs......................: 2087    111.869293/s
     iteration_duration.............: avg=6.74s    min=1.23s    med=7.98s   max=11.18s   p(90)=8.93s    p(95)=9.02s
     iterations.....................: 2087    111.869293/s
     vus............................: 21      min=21       max=1000
     vus_max........................: 1000    min=1000     max=1000


running (18.7s), 0000/1000 VUs, 2087 complete and 0 interrupted iterations
default ✓ [ 100% ] 1000 VUs  10s


-------------------------------------------------------------------------------------------------------------------------------
## SpringMvc - 2000vus - 10s
-------------------------------------------------------------------------------------------------------------------------------
running (25.6s), 0000/2000 VUs, 3119 complete and 0 interrupted iterations
default ✓ [ 100% ] 2000 VUs  10s

     ✓ status is 200

     checks.........................: 100.00% ✓ 3119       ✗ 0
     data_received..................: 393 kB  15 kB/s
     data_sent......................: 299 kB  12 kB/s
     http_req_blocked...............: avg=510.37ms min=840ns    med=684.48ms max=1.11s    p(90)=992.89ms p(95)=1s
     http_req_connecting............: avg=387.97ms min=0s       med=524.98ms max=1.02s    p(90)=769.39ms p(95)=772.44ms
     http_req_duration..............: avg=9.81s    min=829.4ms  med=11.58s   max=18.03s   p(90)=14.97s   p(95)=15.4s
       { expected_response:true }...: avg=9.81s    min=829.4ms  med=11.58s   max=18.03s   p(90)=14.97s   p(95)=15.4s
     http_req_failed................: 0.00%   ✓ 0          ✗ 3119
     http_req_receiving.............: avg=865.27µs min=10.37µs  med=49.25µs  max=171.88ms p(90)=375.5µs  p(95)=3.05ms
     http_req_sending...............: avg=422.93µs min=3.43µs   med=31.96µs  max=13.32ms  p(90)=1.16ms   p(95)=2.14ms
     http_req_tls_handshaking.......: avg=0s       min=0s       med=0s       max=0s       p(90)=0s       p(95)=0s
     http_req_waiting...............: avg=9.81s    min=828.72ms med=11.58s   max=18.03s   p(90)=14.97s   p(95)=15.4s
     http_reqs......................: 3119    121.761963/s
     iteration_duration.............: avg=11.32s   min=2.06s    med=13.53s   max=19.03s   p(90)=16s      p(95)=16.64s
     iterations.....................: 3119    121.761963/s
     vus............................: 57      min=57       max=2000
     vus_max........................: 2000    min=2000     max=2000


running (25.6s), 0000/2000 VUs, 3119 complete and 0 interrupted iterations
default ✓ [ 100% ] 2000 VUs  10s


-------------------------------------------------------------------------------------------------------------------------------
## Spring-webflux - 500vus - 10s
-------------------------------------------------------------------------------------------------------------------------------
running (13.9s), 014/500 VUs, 1528 complete and 0 interrupted iterations
default ↓ [ 100% ] 500 VUs  10s

     ✓ status is 200

     checks.........................: 100.00% ✓ 1542       ✗ 0
     data_received..................: 148 kB  10 kB/s
     data_sent......................: 148 kB  10 kB/s
     http_req_blocked...............: avg=64.92ms min=900ns    med=3.38µs   max=358.81ms p(90)=270.5ms  p(95)=291.48ms
     http_req_connecting............: avg=44.55ms min=0s       med=0s       max=278.6ms  p(90)=148.05ms p(95)=159.31ms
     http_req_duration..............: avg=2.76s   min=204.02ms med=3.01s    max=5.95s    p(90)=3.86s    p(95)=3.9s
       { expected_response:true }...: avg=2.76s   min=204.02ms med=3.01s    max=5.95s    p(90)=3.86s    p(95)=3.9s
     http_req_failed................: 0.00%   ✓ 0          ✗ 1542
     http_req_receiving.............: avg=4.79ms  min=10.73µs  med=156.32µs max=53.32ms  p(90)=17.98ms  p(95)=22.59ms
     http_req_sending...............: avg=86.42µs min=4.32µs   med=12.43µs  max=38.88ms  p(90)=99.45µs  p(95)=233.47µs
     http_req_tls_handshaking.......: avg=0s      min=0s       med=0s       max=0s       p(90)=0s       p(95)=0s
     http_req_waiting...............: avg=2.75s   min=203.73ms med=3s       max=5.95s    p(90)=3.85s    p(95)=3.89s
     http_reqs......................: 1542    107.895662/s
     iteration_duration.............: avg=3.82s   min=1.32s    med=4.01s    max=7.11s    p(90)=4.86s    p(95)=4.9s
     iterations.....................: 1542    107.895662/s
     vus............................: 14      min=14       max=500
     vus_max........................: 500     min=500      max=500


running (14.3s), 000/500 VUs, 1542 complete and 0 interrupted iterations
default ✓ [ 100% ] 500 VUs  10s


-------------------------------------------------------------------------------------------------------------------------------
Spring-webflux - 1000vus - 10s
-------------------------------------------------------------------------------------------------------------------------------
running (16.8s), 0097/1000 VUs, 2006 complete and 0 interrupted iterations
default ↓ [ 100% ] 1000 VUs  10s

     ✓ status is 200

     checks.........................: 100.00% ✓ 2103      ✗ 0
     data_received..................: 202 kB  11 kB/s
     data_sent......................: 202 kB  11 kB/s
     http_req_blocked...............: avg=210.66ms min=890ns    med=5.27µs   max=699.65ms p(90)=583.44ms p(95)=625.64ms
     http_req_connecting............: avg=97.65ms  min=0s       med=0s       max=597.12ms p(90)=290.83ms p(95)=313.56ms
     http_req_duration..............: avg=5.35s    min=384.78ms med=6.66s    max=9.02s    p(90)=6.99s    p(95)=7.01s
       { expected_response:true }...: avg=5.35s    min=384.78ms med=6.66s    max=9.02s    p(90)=6.99s    p(95)=7.01s
     http_req_failed................: 0.00%   ✓ 0         ✗ 2103
     http_req_receiving.............: avg=9.45ms   min=9.56µs   med=127.55µs max=121.62ms p(90)=29.48ms  p(95)=48.99ms
     http_req_sending...............: avg=561.7µs  min=4.3µs    med=20.24µs  max=17.01ms  p(90)=1.13ms   p(95)=3.99ms
     http_req_tls_handshaking.......: avg=0s       min=0s       med=0s       max=0s       p(90)=0s       p(95)=0s
     http_req_waiting...............: avg=5.34s    min=380.84ms med=6.66s    max=9s       p(90)=6.99s    p(95)=7s
     http_reqs......................: 2103    118.22538/s
     iteration_duration.............: avg=6.57s    min=1.66s    med=7.66s    max=10.02s   p(90)=8.01s    p(95)=8.38s
     iterations.....................: 2103    118.22538/s
     vus............................: 97      min=97      max=1000
     vus_max........................: 1000    min=1000    max=1000


running (17.8s), 0000/1000 VUs, 2103 complete and 0 interrupted iterations
default ✓ [ 100% ] 1000 VUs  10s



-------------------------------------------------------------------------------------------------------------------------------
## Spring-webflux - 2000vus - 10s
-------------------------------------------------------------------------------------------------------------------------------
running (24.6s), 0008/2000 VUs, 3168 complete and 0 interrupted iterations
default ↓ [ 100% ] 2000 VUs  10s

     ✓ status is 200

     checks.........................: 100.00% ✓ 3176       ✗ 0
     data_received..................: 305 kB  12 kB/s
     data_sent......................: 305 kB  12 kB/s
     http_req_blocked...............: avg=478.31ms min=830ns    med=579.65ms max=1.19s    p(90)=1.02s    p(95)=1.09s
     http_req_connecting............: avg=347.63ms min=0s       med=403.41ms max=1.05s    p(90)=761.04ms p(95)=832.91ms
     http_req_duration..............: avg=9.38s    min=823.04ms med=10.74s   max=17.02s   p(90)=13.93s   p(95)=13.96s
       { expected_response:true }...: avg=9.38s    min=823.04ms med=10.74s   max=17.02s   p(90)=13.93s   p(95)=13.96s
     http_req_failed................: 0.00%   ✓ 0          ✗ 3176
     http_req_receiving.............: avg=11.38ms  min=10.7µs   med=78.01µs  max=191.02ms p(90)=31.64ms  p(95)=56.21ms
     http_req_sending...............: avg=108.65µs min=3.78µs   med=24.98µs  max=7.02ms   p(90)=167.17µs p(95)=467.11µs
     http_req_tls_handshaking.......: avg=0s       min=0s       med=0s       max=0s       p(90)=0s       p(95)=0s
     http_req_waiting...............: avg=9.37s    min=822.59ms med=10.72s   max=17.02s   p(90)=13.92s   p(95)=13.95s
     http_reqs......................: 3176    128.386214/s
     iteration_duration.............: avg=10.86s   min=2.04s    med=12.65s   max=18.02s   p(90)=14.95s   p(95)=14.99s
     iterations.....................: 3176    128.386214/s
     vus............................: 8       min=8        max=2000
     vus_max........................: 2000    min=2000     max=2000


running (24.7s), 0000/2000 VUs, 3176 complete and 0 interrupted iterations
default ✓ [ 100% ] 2000 VUs  10s


### Durante nossos testes com as bibliotecas Spring MVC e Spring WebFlux, notamos uma diferença significativa no uso de threads. O Spring MVC utiliza uma quantidade exorbitante de threads para processar solicitações bloqueantes, enquanto o Spring WebFlux é mais eficiente e utiliza uma quantidade menor de threads para processar solicitações não bloqueantes. O Spring MVC pode ter problemas de escalabilidade e desempenho devido ao uso excessivo de threads, enquanto o Spring WebFlux é mais leve e ágil em sua abordagem para processar solicitações.

### Em resumo, a escolha entre Spring MVC e Spring WebFlux depende do tipo de aplicação que está sendo construída e das necessidades específicas de desempenho e escalabilidade. Se a aplicação precisar lidar com um grande número de solicitações simultâneas ou precisar ter um alto desempenho, o Spring WebFlux pode ser a melhor escolha. Já se a aplicação não tiver requisitos de alto desempenho e escalabilidade, o Spring MVC pode ser uma opção mais simples e fácil de usar.

