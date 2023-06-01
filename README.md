Performance comparison of `next` and `nuxt` with minimal hello world example. These benchmarks are based on the production build of both the meta frameworks.

Here are the visuals (— thanks to [@icarusgk](https://twitter.com/icarusgkx)):
![total requeets](https://pbs.twimg.com/media/FxfE2dTXsAEpaJm?format=jpg&name=4096x4096)
![avg response time](https://pbs.twimg.com/media/FxfFXOeWYAQ1UyH?format=jpg&name=4096x4096)

Program used for benchmarks:
- `oha`

Nuxtjs benchmarks
```bash
$ oha -z 10s http://localhost:3000
Summary:
  Success rate: 1.0000
  Total:        10.0010 secs
  Slowest:      0.0488 secs
  Fastest:      0.0026 secs
  Average:      0.0081 secs
  Requests/sec: 6134.8161

  Total data:   42.13 MiB
  Size/request: 720 B
  Size/sec:     4.21 MiB

Response time histogram:
  0.003 [1]     |
  0.007 [29637] |■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■
  0.012 [24751] |■■■■■■■■■■■■■■■■■■■■■■■■■■
  0.016 [4301]  |■■■■
  0.021 [1430]  |■
  0.026 [878]   |
  0.030 [214]   |
  0.035 [75]    |
  0.040 [12]    |
  0.044 [2]     |
  0.049 [53]    |

Latency distribution:
  10% in 0.0051 secs
  25% in 0.0055 secs
  50% in 0.0074 secs
  75% in 0.0091 secs
  90% in 0.0125 secs
  95% in 0.0153 secs
  99% in 0.0239 secs

Details (average, fastest, slowest):
  DNS+dialup:   0.0010 secs, 0.0003 secs, 0.0016 secs
  DNS-lookup:   0.0000 secs, 0.0000 secs, 0.0005 secs

Status code distribution:
  [200] 61354 responses
```

Nextjs benchmarks
```bash
$ oha -z 10s http://localhost:4000
Summary:
  Success rate: 1.0000
  Total:        10.0005 secs
  Slowest:      0.3962 secs
  Fastest:      0.0271 secs
  Average:      0.0440 secs
  Requests/sec: 1134.8390

  Total data:   5.65 MiB
  Size/request: 522 B
  Size/sec:     578.50 KiB

Response time histogram:
  0.027 [1]     |
  0.064 [11014] |■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■
  0.101 [284]   |
  0.138 [0]     |
  0.175 [0]     |
  0.212 [0]     |
  0.249 [0]     |
  0.285 [0]     |
  0.322 [0]     |
  0.359 [24]    |
  0.396 [26]    |

Latency distribution:
  10% in 0.0333 secs
  25% in 0.0364 secs
  50% in 0.0408 secs
  75% in 0.0468 secs
  90% in 0.0549 secs
  95% in 0.0595 secs
  99% in 0.0750 secs

Details (average, fastest, slowest):
  DNS+dialup:   0.0001 secs, 0.0000 secs, 0.0009 secs
  DNS-lookup:   0.0000 secs, 0.0000 secs, 0.0003 secs

Status code distribution:
  [200] 11349 responses
```

