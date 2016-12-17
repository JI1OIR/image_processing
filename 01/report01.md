#課題１レポート　標本化間隔と空間解像度  
・画像をダウンサンプリングして（標本化間隔を大きくして）表示せよ  
  
ORG=imread('ip_img.jpg');  
imagesc(ORG); axis image;  
  
上記によりMATLABに画像を読み込み，表示させた結果を図１に示す．  
  
![原画像](https://github.com/JI1OIR/image_processing/blob/master/01/org.png?raw=true)  
図１ オリジナル画像  
  
この画像をダウンサンプリングする．1/2倍に縮小し，2倍に拡大することによってダウンサンプリングすることができる．  
IMG = imresize(ORG,0.5);  
IMG2 = imresize(IMG,2,'box');  
上記を実行した結果の画像を図２に示す  
![原画像](https://github.com/JI1OIR/image_processing/blob/master/01/im1.png?raw=true)  
図２ 1/2ダウンサンプリング  
  
続いて1/4サンプリングを行う．1/4倍に縮小し，4倍に拡大して表示させる．  

IMG = imresize(ORG,0.25); % 画像の縮小  
IMG2 = imresize(IMG,4,'box');  
上記を実行した結果を図３に示す． 
  
![原画像](https://github.com/JI1OIR/image_processing/blob/master/01/im2.png?raw=true)  
図３ 1/4ダウンサンプリング  

同じようにして1/8，1/16，1/32サンプリングし，その実行結果の画像をそれぞれ図４，図５，図６に示す．
  
![原画像](https://github.com/JI1OIR/image_processing/blob/master/01/im3.png?raw=true)  
図４ 1/8ダウンサンプリング  
  
![原画像](https://github.com/JI1OIR/image_processing/blob/master/01/im4.png?raw=true)  
図５ 1/16ダウンサンプリング  
  
![原画像](https://github.com/JI1OIR/image_processing/blob/master/01/im5.png?raw=true)  
図６ 1/32ダウンサンプリング    

・考察  
実行結果より，縮小と拡大によるダウンサンプリングを行うとモザイク状のサンプリング歪みが生じる．
