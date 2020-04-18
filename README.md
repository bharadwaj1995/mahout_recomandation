# Apache Mahout
## 44517 Sec 01, Bigdata
### Workshop 06
### Team Members
* Subrahmanya Sai Bharadwaj Gandrakota
* Sowmya Reddy Kumbham
* Bhuvanesh Nakka
* Sneha Madhavaram

Step 1: Create DataModel Object

DataModel datamodel = new FileDataModel(new File("input file"));

Step 2: Create UserSimilarity Object

UserSimilarity similarity = new PearsonCorrelationSimilarity(datamodel);

Step 3: Create UserNeighborhood object

UserNeighborhood neighborhood = new ThresholdUserNeighborhood(3.0, similarity, model);

Step 4: Create Recommender Object

UserBasedRecommender recommender = new GenericUserBasedRecommender(model, neighborhood, similarity);

Step5: Recommend Items to a User

List<RecommendedItem> recommendations = recommender.recommend(2, 3);

for (RecommendedItem recommendation : recommendations) {
   System.out.println(recommendation);
 }
 
 
 
##### Compile the java program : javac Recommender.java
##### Run The java program : java Recommender


