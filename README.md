# 鉴定流程
参考 https://plantcode.cup.uni-freiburg.de/tapscan/index.php 获得各TAP的Domain rules，并根据规则鉴定

# 使用方法
## 第一步
运行hmmscan，鉴定结构域，请添加--domtblout，例如
```
hmmscan --domtblout hmmscan_out -E 1e-5 --cpu 10 TAPFinder.hmm Ath.pep.fa
```
## 第二步
1. 在Linux系统直接执行，不用额外配置环境
3. 执行如下命令查看使用方法
```
./TAPFinder.bin -h
```
例如
```
TAPFinder/TAPFinder.bin --pep Ath.pep.fa --rules TAPFinder/TAPs_domain_rules.tsv --domain_coverage_cutoffs TAPFinder/domain_coverage_cutoffs.tsv --hmmscan_out hmmscan.out.tsv --score_cutoff 0 --processing 10
```

# 结果解读
TAPFinder.final.out.tsv 包含6列
1. 基因编号
2. 所属 TAP id
3. 所属 TAP 名称
4. 按规则该 TAP 需要具备的结构域
5. 按规则该 TAP 不能具备的结构域
6. 该基因实际鉴定到的结构域

# 参考文献
Wilhelmsson, Per K.I., Cornelia Mühlich, Kristian K. Ullrich和Stefan A. Rensing. 《Comprehensive Genome-Wide Classification Reveals That Many Plant-Specific Transcription Factors Evolved in Streptophyte Algae》. Genome Biology and Evolution 9, 期 12 (2017年): 3384–97. https://doi.org/10.1093/gbe/evx258.
