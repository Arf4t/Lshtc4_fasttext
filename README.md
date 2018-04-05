# Lshtc_fasttext
Using fasttext to classify lshtc training data(for model evaluation ). 
(As true labels are not present for lshtc test data)
 
 **Lshtc has 325,056 categories.**
 <p>As the number of categories are high in lshtc . I'm trying to check the performance of fasttext for the top n categories present in the lshtc training data.</p>
 <p> Here, I'm checking for n=10,100,1000,10000</p>
 <p> The observation is that as no. of categories increases the performance decreases. Here, performance is measured on basis of macro_f1_score.</p>

**Fasttext parameters used are :**
    <p>dim 200 , epoch 100 , lr 0.25 , loss hs </p>
    <p> The number of labels predicted by fastext is based on the Average_labels_per_document in top n class data</p>
    <p>The results are as follows:</p>

**for n=10:**
  Average_labels_per_document in top 10 class data is 1.2040520887536859

So,Predicting  1 labels using fasttext

For top 10 class (precision,recall,fscore) using macro average: (0.7721319410090449, 0.45440001895511434, 0.544640031905407, None)

**for n=100:**

Average_labels_per_document in top 100 class data is 1.4025902858246426

So,Predicting  1 labels using fasttext

For top 100 class (precision,recall,fscore) using macro average: (0.5063146170884429, 0.2950444835595893, 0.3544236294610442, None)

**for n=1000:**

Average_labels_per_document in top 1000 class data is 1.9115519552849054

So,Predicting  2 labels using fasttext

For top 1000 class (precision,recall,fscore) using macro average: (0.3455700747447608, 0.3395190123331962, 0.3231711861919399, None)

**for n=10000:**

Average_labels_per_document in top 10000 class data is 2.4095504116927997

So,Predicting  2 labels using fasttext

For top 10000 class (precision,recall,fscore) using macro average: (0.2500700256356269, 0.22185674621604384, 0.2148148932757374, None)
