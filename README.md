# Lshtc_fasttext
Using fasttext to classify lshtc training data(for model evaluation ). 
(As true labels are not present for lshtc test data)
 
 <h2>Lshtc has 325,056 categories.</h2>
 
 

 <p>As the number of categories are high in lshtc . I'm trying to check the performance of fasttext for the top n categories present in the lshtc training data.</p>
 <p> Here, I'm checking for n=10,100,1000,10000</p>
 <p> The observation is that as no. of categories increases the performance decreases. Here, performance is measured on basis of **macro_f1_score.</p>


 <h2>Note</h2>
 <p> Here, lshtc training data ( for each n ) is built based on only top n labels</p>
 
 <p>For each n , the lshtc training data is divided into train(70%) & test (30%) sets by shuffling </p>
 
 
 <h2>Fasttext parameters used are :</h2>
    <p>dim 200 , epoch 100 , lr 0.25 , loss hs </p>
    <p> The number of labels predicted by fastext is based on the Average_labels_per_document in top n class data</p>
    <p>The results are as follows:</p>

<h2>for n=10:</h2>
  
  **Average_labels_per_document** = 1.2040520887536859

So,Predicting  1 label per doc using fasttext

**macro_precision** = 0.7721319410090449

**macro_recall** = 0.45440001895511434

**macro_fscore** = 0.544640031905407

<h2>for n=100:</h2>

**Average_labels_per_document** = 1.4025902858246426

So,Predicting  1 label per doc using fasttext


**macro_precision** = 0.5063146170884429

**macro_recall** = 0.2950444835595893

**macro_fscore** = 0.3544236294610442


<h2>for n=1000:</h2>

**Average_labels_per_document** = 1.9115519552849054

So,Predicting  2 labels per doc using fasttext

**macro_precision** = 0.3455700747447608

**macro_recall** = 0.3395190123331962

**macro_fscore** = 0.3231711861919399


<h2>for n=10000:</h2>

**Average_labels_per_document** = 2.4095504116927997

So,Predicting  2 labels per doc using fasttext

**macro_precision** = 0.2500700256356269

**macro_recall** = 0.22185674621604384

**macro_fscore** = 0.2148148932757374

