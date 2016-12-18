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

![原画像](https://github.com/JI1OIR/image_processing/blob/master/02/02im2.png?raw=true)  

図３  

![原画像](https://github.com/JI1OIR/image_processing/blob/master/02/02im3.png?raw=true)  

図４    
  
