# 鉴定流程
参考 https://plantcode.cup.uni-freiburg.de/tapscan/index.php 获得各TAP的Domain rules，并根据规则鉴定

# 使用方法
1. 在Linux系统直接执行，不用额外配置环境
2. 环境中可执行 hmmscan
3. 执行如下命令查看使用方法
```
./TAPFinder.bin -h
```
例如
```
TAPFinder/TAPFinder.bin --pep Ath.pep.fa --rules TAPFinder/TAPs_domain_rules.tsv --domain_coverage_cutoffs TAPFinder/domain_coverage_cutoffs.tsv --hmm TAPFinder/TAPFinder_hmm/TAPFinder.hmm --score_cutoff 0 --processing 10
```

# 结果解读
TAPFinder.final.out.tsv 包含6列
1. 基因编号
2. 所属 TAP id
3. 所属 TAP 名称
4. 按规则该 TAP 需要具备的结构域
5. 按规则该 TAP 不能具备的结构域
6. 该基因实际鉴定到的结构域