## Learning lightcurve analysis (work at ./ipynb)

## 1. Prepartion
-  Install python & Jupyter  
-  Anaconda may be the easiest way to install python, Jupyter, and other modules  
https://docs.anaconda.com/anaconda/install/


## 2. Install python modules
### 2.1 List of requsite modules
1. lightkurve (https://docs.lightkurve.org/quickstart.html)  
2. batman (https://lweb.cfa.harvard.edu/~lkreidberg/batman/)  
3. lmfit (https://lmfit.github.io/lmfit-py/)  
4. numpy, matplotlib, scipy (automatically installed through anaconda)

### 2.2 how to install modules
#### (a) If you want to install ##,  
**conda install ##**  

#### (b) If modules cannot be install by (a), search in another repository,  
**conda install -c conda-forge ##** (to see another repository.)  
 
#### (c) If modules cannot be install by (a) & (b), use pip
**pip install ##**  
(pip & anaconda are sometimes interfered with each other, so you should be carefule about that. )

## 3. 走らせる
2で作成したc_compile_ring.soをimportすれば使用できる。  
exoring_testフォルダに使用例(fit_test.py)を載せた。  
- python fit_test.py  

と打てば動く。このコードでは、実際にAizawa+2017で解析したデータ(Q8_l_KIC10403228_test_detrend.dat)を読み込み
それと指定したパラメータ (para_result_ring.datの2列目)でのモデルフラックスを並べてplotしてくれる。  

## 番外編 (./c_ext)
c_extフォルダでは実際にcを用いたフィッティングなどを行ってくれる。  
gslをインストールした後に、  
- gcc main.c mpfit.c -lgsl -lgslcblas  

として作成した実行ファイルを実行するとフィティングまでしてくれる。  
