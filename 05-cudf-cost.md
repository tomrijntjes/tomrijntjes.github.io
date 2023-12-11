# cuDF Cost

Which VM is most cost-effective for cuDF?

Among the CompuBench tests, the "N-Body simulation" benchmarks are likely the most relevant for predicting cuDF performance. These tests involve complex calculations and data manipulations similar to operations performed in cuDF, which is designed for data frame manipulation and analysis. 


![](./img/gpu-cost-vs-performance-nbody.png)

| GPU        | AWS $ per hour | Azure $ per hour | Google Cloud | Min   | N-Body simulation – 128k - iterations/s | iterations/h | $/billion iterations |
|------------|----------------|------------------|--------------|-------|-----------------------------------------|--------------|----------------------|
| K80        |                |              0,9 |         0,85 |  0,85 |                                   25121 |     90435600 |          9,398953509 |
| T4         |            1,2 |              1,2 |         0,75 |  0,75 |                                   54082 |    194695200 |          3,852175092 |
| P100       |                |             2,07 |         1,86 |  1,86 |                                   83053 |    298990800 |          6,220927199 |
| V100 16 GB |           3,06 |             3,06 |         2,88 |  2,88 |                                  123497 |    444589200 |          6,477890151 |
| A100 40 GB |          4,100 |            3,400 |         3,67 | 3,400 |                                  170915 |    615294000 |          5,525813676 |


## Sources

1. Pricing data from [paperspace](https://www.paperspace.com/gpu-cloud-comparison)
1. Benchmarks from [Compubench](https://compubench.com)