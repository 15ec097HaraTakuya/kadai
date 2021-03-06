# 課題1  
ここではMATLABを用いて標本化間隔による解像度の違いを確認する。  
まず、MATLABに画像を読み込み表示する。  
読み込み用にimread関数を、表示用にimage(sc)関数を用いて以下の様に記述する。  
  
ORG = imread('Nuko.jpg');%画像をIMG変数に格納  
image(ORG);%IMGを表示  
  
ここでは、次の800×533の画像Nuko.jpgを使う。  
![Alt text](MATLAB/Nuko.jpg)  
図1　使用原画像  
原画像を1/2サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい。  
よって、imresize関数と「box」オプションを用いて次のように記述する。  
  
IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大  
  
1/2サンプリングの結果を図２に示す。  
![Alt text](MATLAB/kadai1/Nuko1.jpg)  
図2　1/2サンプリング  
  
同様に原画像を1/4サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい。  
よって次のように記述する。  　
  
IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,4,'box'); % 画像の拡大  
  
1/4サンプリングの結果を図３に示す。  
![Alt text](MATLAB/kadai1/Nuko2.jpg)  
図3　1/4サンプリング  
  
以降1/8から1/32まで繰り返し行う。  
サンプリングの結果を図４～６に示す。
![Alt text](MATLAB/kadai1/Nuko3.jpg)  
図4　1/8サンプリング 
![Alt text](MATLAB/kadai1/Nuko4.jpg)  
図5　1/16サンプリング 
![Alt text](MATLAB/kadai1/Nuko5.jpg)  
図6　1/32サンプリング 
