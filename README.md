Performance comparison of `next`, `nuxt` and `sveltekit` with minimal hello world example. These benchmarks are based on the production build of all the meta frameworks.

Program used for benchmarks:

- `oha`

All benchmarks were rerun on my machine _MacBook Pro, Apple M2 Max, 32 GB memory_.

Nuxtjs benchmarks

```bash
$ oha -z 10s http://localhost:3000
Summary:
  Success rate:	1.0000
  Total:	10.0004 secs
  Slowest:	0.0301 secs
  Fastest:	0.0002 secs
  Average:	0.0041 secs
  Requests/sec:	12254.5125

  Total data:	84.15 MiB
  Size/request:	720 B
  Size/sec:	8.41 MiB

Response time histogram:
  0.000 [1]     |
  0.003 [28025] |■■■■■■■■■■
  0.006 [86144] |■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■
  0.009 [4986]  |■
  0.012 [2871]  |■
  0.015 [317]   |
  0.018 [142]   |
  0.021 [6]     |
  0.024 [0]     |
  0.027 [51]    |
  0.030 [7]     |

Latency distribution:
  10% in 0.0031 secs
  25% in 0.0032 secs
  50% in 0.0036 secs
  75% in 0.0043 secs
  90% in 0.0047 secs
  95% in 0.0074 secs
  99% in 0.0102 secs

Details (average, fastest, slowest):
  DNS+dialup:	0.0017 secs, 0.0013 secs, 0.0024 secs
  DNS-lookup:	0.0001 secs, 0.0000 secs, 0.0005 secs

Status code distribution:
  [200] 122550 responses
```

Nextjs benchmarks

```bash
$ oha -z 10s http://localhost:4000
Summary:
  Success rate:	1.0000
  Total:	10.0017 secs
  Slowest:	6.7320 secs
  Fastest:	0.0011 secs
  Average:	0.0446 secs
  Requests/sec:	547.2075

  Total data:	2.73 MiB
  Size/request:	524 B
  Size/sec:	280.02 KiB

Response time histogram:
  0.001 [1]    |
  0.674 [5453] |■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■
  1.347 [0]    |
  2.020 [0]    |
  2.693 [0]    |
  3.367 [0]    |
  4.040 [0]    |
  4.713 [0]    |
  5.386 [0]    |
  6.059 [0]    |
  6.732 [19]   |

Latency distribution:
  10% in 0.0131 secs
  25% in 0.0139 secs
  50% in 0.0155 secs
  75% in 0.0184 secs
  90% in 0.0221 secs
  95% in 0.0260 secs
  99% in 0.3419 secs

Details (average, fastest, slowest):
  DNS+dialup:	0.0001 secs, 0.0000 secs, 0.0019 secs
  DNS-lookup:	0.0000 secs, 0.0000 secs, 0.0001 secs

Status code distribution:
  [200] 5473 responses
```

SvelteKit benchmarks

```bash
$ oha -z 10s http://localhost:4173
Summary:
  Success rate:	1.0000
  Total:	10.0005 secs
  Slowest:	0.0615 secs
  Fastest:	0.0100 secs
  Average:	0.0147 secs
  Requests/sec:	3393.1405

  Total data:	27.28 MiB
  Size/request:	843 B
  Size/sec:	2.73 MiB

Response time histogram:
  0.010 [1]     |
  0.015 [29621] |■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■
  0.020 [2571]  |■■
  0.025 [645]   |
  0.031 [883]   |
  0.036 [136]   |
  0.041 [26]    |
  0.046 [17]    |
  0.051 [13]    |
  0.056 [10]    |
  0.062 [10]    |

Latency distribution:
  10% in 0.0134 secs
  25% in 0.0136 secs
  50% in 0.0139 secs
  75% in 0.0142 secs
  90% in 0.0159 secs
  95% in 0.0206 secs
  99% in 0.0285 secs

Details (average, fastest, slowest):
  DNS+dialup:	0.0021 secs, 0.0015 secs, 0.0026 secs
  DNS-lookup:	0.0000 secs, 0.0000 secs, 0.0001 secs

Status code distribution:
  [200] 33933 responses
```
