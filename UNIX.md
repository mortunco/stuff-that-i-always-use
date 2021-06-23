# stuff-that-i-always-use
### downloading bigwigs from chip-atlas

```
Create a file like this. file name SRX
22Rv1-AR-totalRNA-DHT-GSM2734938  SRX3068918
22Rv1-AR-totalRNA-DHT-GSM2734939	SRX3068919
22Rv1-AR-siv7-DHT-GSM2734940	SRX3068920
```
```
## both hg19
cat download  | parallel --col-sep="\t" "wget -O {1}.bigwig http://dbarchive.biosciencedbc.jp/kyushu-u/hg19/eachData/bw/{2}.bw"

### qvalue 0.05
cat download  | parallel --col-sep="\t" "wget -O {1}.bigwig http://dbarchive.biosciencedbc.jp/kyushu-u/hg19/eachData/bw/{2}.05.bed"
```
