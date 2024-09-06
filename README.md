# chatPDF
## install
### pdf2markdown
+ https://tools.textin.com/transform/pdf2markdown 效果优秀
### 本地替代 （效果不佳）
```powershell
conda create -n markerPdf pytorch torchvision torchaudio pytorch-cuda=12.4 -c pytorch -c nvidia
conda activate markerPdf
pip install marker-pdf -i https://pypi.tuna.tsinghua.edu.cn/simple

# 大约需要下载 154M + 154M + 550M + 941M + 625M 五个模型，峰值显存占用 5 G， 60% 的准确率吧
$env:HF_ENDPOINT="https://hf-mirror.com"; marker_single test.pdf test --batch_multiplier 1

marker /path/to/input/folder /path/to/output/folder --workers 1 --min_length 5000
```
