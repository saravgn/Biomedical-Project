##WEB SERVER

- **CREATE THE DIRECTORY** **data\.db** where MongoDb will save datas lately

- **RUN MONGODB** from the directory D:\Biomedica\mongodb\bin and give it the directory created above to save datas

#figura1

-**POPULATE THE DB** giving to the partitioner.py the file bone0.txt

#figura2


-in order to verify if everything is succesfull with Mongodb run its client-side
 you can find an **existing id** to give to "retreive-cluster.py"


#figura3


**retreive-clusters.py**

    import json
    from pymongo import MongoClient

    client = MongoClient('localhost', 27017)
    db = client['db-bio']
    clusters = db.clusters
    
    '''the method clusters.find_one takes as imput the fixed id-string '''
    
    data = json.dumps(clusters.find_one({"_id": "011"}), indent=2)
    print("Content-type:application/json\n")
    print(data)
    
    
    
    
-here it is the web server

#figura4

#figura5


