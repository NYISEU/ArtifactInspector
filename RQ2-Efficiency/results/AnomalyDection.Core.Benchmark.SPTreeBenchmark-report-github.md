```

BenchmarkDotNet v0.13.12, Windows 10 (10.0.19045.4170/22H2/2022Update)
Intel Core i3-4160 CPU 3.60GHz (Haswell), 1 CPU, 4 logical and 2 physical cores
.NET SDK 8.0.200
  [Host] : .NET 8.0.2 (8.0.224.6711), X64 RyuJIT AVX2
  Dry    : .NET 8.0.2 (8.0.224.6711), X64 RyuJIT AVX2

Job=Dry  IterationCount=20  LaunchCount=1  
RunStrategy=ColdStart  UnrollFactor=1  WarmupCount=5  

```
| Method       | Mean      | Error      | StdDev     | Median   | Min       | Max       | Gen0       | Gen1      | Allocated   |
|------------- |----------:|-----------:|-----------:|---------:|----------:|----------:|-----------:|----------:|------------:|
| PrevApproach | 190.80 ms | 217.063 ms | 249.970 ms | 77.49 ms | 0.4519 ms | 846.13 ms | 13000.0000 | 1000.0000 | 802570.2 KB |
| OurApproach  |  11.77 ms |   4.058 ms |   4.673 ms | 13.45 ms | 0.4004 ms |  17.44 ms |          - |         - |    85.16 KB |
