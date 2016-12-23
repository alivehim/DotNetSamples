``` ini

BenchmarkDotNet=v0.10.1, OS=OSX
Processor=?, ProcessorCount=4
Frequency=1000000000 Hz, Resolution=1.0000 ns, Timer=UNKNOWN
dotnet cli version=1.0.0-preview2-1-003177
  [Host]     : .NET Core 4.6.24628.01, 64bit RyuJIT
  DefaultJob : .NET Core 4.6.24628.01, 64bit RyuJIT


```
             Method |           Mean |      StdErr |        StdDev |         Median |    Gen 0 |    Gen 1 |    Gen 2 | Allocated |
------------------- |--------------- |------------ |-------------- |--------------- |--------- |--------- |--------- |---------- |
        WithLinq100 |      4.5519 us |   0.0191 us |     0.0740 us |      4.5367 us |   2.5523 |        - |        - |    4.3 kB |
     WithoutLinq100 |      3.2431 us |   0.0269 us |     0.1006 us |      3.2063 us |   0.9918 |        - |        - |   1.85 kB |
      WithLinq10000 |    611.6177 us |   1.9356 us |     6.9789 us |    610.4871 us | 211.4258 |  68.8477 |  68.8477 |  517.8 kB |
   WithoutLinq10000 |    358.2175 us |   1.2289 us |     4.7596 us |    357.5338 us |  50.5859 |  25.0651 |  25.0651 | 158.31 kB |
     WithLinq100000 |  6,837.4189 us |  37.9723 us |   142.0795 us |  6,807.7043 us | 708.3333 | 583.3333 | 581.2500 |   4.07 MB |
  WithoutLinq100000 |  4,535.0311 us |  18.7528 us |    67.6143 us |  4,510.0612 us | 187.5000 | 187.5000 | 187.5000 |    1.2 MB |
     WithLinq500000 | 49,422.2958 us | 190.8018 us |   738.9720 us | 49,415.8006 us | 416.6667 | 291.6667 | 291.6667 |  13.92 MB |
  WithoutLinq500000 | 42,026.4738 us | 573.6189 us | 5,501.9594 us | 39,516.0321 us | 120.8333 | 120.8333 | 120.8333 |   5.61 MB |
    WithLinq1000000 |  6,862.8489 us |  20.7542 us |    74.8304 us |  6,855.2981 us | 772.9167 | 639.5833 | 639.5833 |   4.07 MB |
 WithoutLinq1000000 |  5,183.1393 us |  70.8731 us |   661.0606 us |  4,914.1731 us | 170.8333 | 170.8333 | 170.8333 |    1.2 MB |