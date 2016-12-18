#課題２レポート　階調数と疑似輪郭  
  
課題２：２階調，４階調，８階調の画像を生成せよ．  
  
グレースケールで2階調の画像を生成する．MATLABにサンプル画像を読み込み，以下の処理を行った．  
  
ORG=imread('Lenna.png'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
  
imagesc(ORG); axis image; % 画像の表示  
その結果を図１に示す．  
![原画像](https://github.com/JI1OIR/image_processing/blob/master/02/02o.png?raw=true)  

図１ グレースケール
  
  
続いて，２階調画像を生成する．以下の処理を行った．  

IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  

この処理の結果を図２に示す．

![原画像](https://github.com/JI1OIR/image_processing/blob/master/02/02im1.png?raw=true)  

図２  ２階調画像
４階調画像を生成する．以下の処理を行った．  

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
  
![原画像](https://github.com/JI1OIR/image_processing/blob/master/02/02im2.png?raw=true)  

図３  ４階調画像  

8階調画像を生成する．以下の処理を行った．  
IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>128;  
IMG3 = ORG>160;  
IMG4 = ORG>192;  
IMG5 = ORG>224;  
IMG6 = ORG>256;  
IMG = IMG0 + IMG1 + IMG2 +IMG3 +IMG4 +IMG5 +IMG6;  

![原画像](https://github.com/JI1OIR/image_processing/blob/master/02/02im3.png?raw=true)  

図４  8階調画像  
  

考察
階調表現は１画素ごとの明るさを数値で表現する．２階調は1bitで２段階，４階調は2bitで４段階，８階調は3bitで８段階であることが上記の処理でわかった．
