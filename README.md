# **HHA504 || Working with Managed No-SQL Databases**
---

#### **🎯** This task is part of my assignment focused on creating and configuring databases in different platforms, such as Google Cloud Platform's BigQuery, MongoDB Atlas, and Redis Cloud.

---

# _*Steps Taken to Complete this Assignment*_

---

## Dataset Overview: 

- _**Link to the dataset used**_: [Fake Dataset](https://raw.githubusercontent.com/hantswilliams/HHA-504-2024/refs/heads/main/other/module8/module8_nosql_hw.csv)
  - Below is an overview to the healthcare dataset that will be uploaded in different platforms.
    
    ```csv
    PatientID,Name,Age,Gender,DiagnosisCode,VisitDate,Hospital,TreatmentPlan,FollowUpDate
    
    1,John Doe,45,M,M54.5,2024-09-10,Stony Brook Hospital,Physical Therapy,2024-09-20
    2,Jane Smith,29,F,E11.9,2024-08-15,Stony Brook Hospital,Insulin,2024-09-15
    3,Bob Johnson,65,M,I10,2024-10-01,Long Island Clinic,Hypertension Medication,2024-11-01
    4,Alice Williams,50,F,J45.909,2024-07-22,Southampton Hospital,Bronchodilators,2024-08-22
    5,Michael Brown,37,M,G43.909,2024-06-12,Stony Brook Hospital,Triptans,
    6,Susan Davis,54,F,I25.10,2024-05-10,Stony Brook Hospital,Statins,2024-06-10
    ```

- _**Dataset Explanation**_:
  
  - _**PatientID**_: Unique identifier for each patient (integer).
  - _**Name**_: Patient's full name (string).
  - _**Age**_: Age of the patient (integer).
  - _**Gender**_: Gender of the patient (string: M or F).
  - _**DiagnosisCode**_: ICD-10 code representing the patient’s diagnosis (string).
  - _**VisitDate**_: Date of the hospital visit (YYYY-MM-DD format).
  - _**Hospital**_: Name of the hospital or clinic where the visit took place (string).
  - _**TreatmentPlan**_: The prescribed treatment plan for the patient (string).
  - _**FollowUpDate**_: Date for a follow-up visit, if applicable (YYYY-MM-DD format).

 ---

# ☞ _**Google BigQuery (GCP):**_

  - Navigated to BigQuery in the Google Cloud Console.
  - Created a new dataset named **`raqs_no_sql`** in **BigQuery**
    
    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/1.png" width="550" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/2.png" width="550" />.

  - Uploaded the provided healthcare dataset (CSV file) into a new table named **`module8_nosql_hw`** within my newly created dataset **`raqs_no_sql`**.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/3.png" width="550" />.
    
    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/4.png" width="550" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/5.png" width="550" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/7.png" width="550" />.

  - Noted the connection details and the BigQuery editor interface.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/BigQuery%20%5Bjob%20details%5D.png" width="480" />.

  - I modified and explored the data. These are the queries that I used to retrieve data in GCP's BigQuery.

    (1)
    ```sql
    SELECT PatientID, Name, Age, DiagnosisCode, Hospital, TreatmentPlan
    FROM 'maraquel-soriano-hha504.raqs_no_sql.module8-nosql-hw
    WHERE Hospital = 'Stony Brook Hospital';
    ```
    (2)
    ```sql
    SELECT *
    FROM 'maraquel-soriano-hha504.raqs_no_sql module8-nosql-hw'
    WHERE Age >40
    ```

  - To get a better view of what I have explored, see the screenshots below.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/9%20-%20my%20own%20query.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/10.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/11%20-%20Age.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/12%20-%20age%20-%20job%20info.png" width="550" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/GCP/13%20-%20age%20-%20query%20job%20details.png" width="400" />.

---

# ☞ _**MongoDB Atlas (Cloud):**_

  - To accomplish this task, I navigated to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) and registered for the free tier using my **`Stony Brook email`**.
  - Created a new database instance named **`module8-nosql-hw`** and with basic configuration settings. I performed this step on the website and using the MongoDB Compass application, which I downloaded to my laptop.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/1.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/1%20copy.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/2.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/3.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/4%20-%20creating%20database.png" width="600" />.
    
  - Inserted the provided healthcare dataset into a collection named **`patienthealthdata`**, which I created when I first started the new database. I ensured each row was converted to a JSON document.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/5%20-%20import%20csv%20file.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/6%20-%20importing%20csv%20file.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/7%20-%20json%20(data%20-%20all-%20showing%20only%20the%20first%202).png" width="650" />.

  - This is the query that I used to retrieve simple patient data in MongoDB Compass.
    ```json
    {
      "Hospital": "Stony Brook Hospital",
      "Age": { "$gt": 30 }
    }
    ```
    
  - I modified and explored the data and ran a simple query to retrieve patient data.
    
    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/8%20-%20json%20(query-hosp%26age)%201.png" width="685" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/9%20-%20json%20(query-hosp%26age)%202.png" width="650" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/MongoDB/10%20-%20json%20(query-hosp%26age)%203.png" width="650" />.

  - Using the MongoDB Compass application, which I downloaded to my laptop, I realized that the CSV file could be converted into a JSON format. I just needed to hover to the right-hand side of the screen and click the curly bracket icon. Each row containing patient data was converted to a JSON format, which looked like this for each patient:
  
     ```json
       {
        "_id": {
          "$oid": "671e7083387ab9818bd8fe31"
        },
        "PatientID": 2,
        "Name": "Jane Smith",
        "Age": 29,
        "Gender": "F",
        "DiagnosisCode": "E11.9",
        "VisitDate": {
          "$date": "2024-08-15T00:00:00.000Z"
        },
        "Hospital": "Stony Brook Hospital",
        "TreatmentPlan": "Insulin",
        "FollowUpDate": {
          "$date": "2024-09-15T00:00:00.000Z"
      }
      }
    ```


# ☞ _**Redis Cloud:**_

  - To accomplish this task, I navigated to [Redis Cloud](https://redis.io/cloud/) and signed up for a free tier account using my **`Stony Brook email`**.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/Redis/1.png" width="400" />.

  - Created a new Redis database instance named **`raqs-nosql-hw`**.
    
    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/Redis/3.png" width="550" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/Redis/4.png" width="550" />.

  - Connected Redis to **`Python`** using **`Visual Studio Code`**.
    
    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/Redis/5%20-%20VSC%20%5Bto%20REDIS%5D.png" width="700" />.

  - I explored the patient data in **`Redis Insight`** after inserting data into Redis using Python in Visual Studio Code. I installed Redis Insight on my laptop after I created a Redis database instance.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/Redis/6%20-%20redis%20%5Bdb1%5D.png" width="650" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/Redis/7%20-%20redis%20%5Bdb%202%5D.png" width="650" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/Redis/9%20-%20no%20edit.png" width="600" />.

    <img src="https://github.com/raqssoriano/HHA504_assignment_nosql_dbs/blob/main/different%20DB%20platforms/Redis/10.png" width="600" />.


---
---

# ☞ _**My Experience and Reflections Working with GCP's BigQuery, MongoDB, and Redis**_

<table>
<thead>
<tr>
<th> </th>
<th>BIGQUERY</th>
<th>MONGODB</th>
<th>REDIS</th>
</tr>
</thead>
<tbody>
<tr>
<td>📌 Setup Process and Configuration </td>
<td>
  (1) Setting up a Database: Creating a new database was straightforward through the Google Cloud Console. <br> <br>

  (2) Dataset Upload: I find that uploading a new dataset was efficiently done fast within the Google Cloud Console. It gave me the option to upload a CSV file from my local machine or through Google Cloud Storage, which I very find convenient. Also, the uploaded data is imported into tables within the dataset, it gave me the option to review it before completing the process. <br>
  
  (3) BigQuery was able to auto-detect the schema, but it still gave me an option to modify it if needed. <br> 
  
  (4) BigQuery can handle large-scale data with auto-scaling. With my recent exposure to GCP, I found that BigQuery was able to manage this large amount of data effectively.<br> </td>
  
<td> (1) Creating a Cluster: Setting up a new cluster in MongoDB Atlas was intuitive, allowing me to choose both cloud providers (such as AWS, GCP, and Azure) and regions.<br> <br>
  
(2) Dataset Upload: I utilized MongoDB Compass, a GUI tool for MongoDB, to upload a CSV file into a 'cluster' to create a healthcare dataset (collection) named 'patienthealthdata.' <br>

(3) Configuration: MongoDB allows setting database users/roles that ensures secured access to the uploaded healthcare dataset.<br> </td>

<td> (1) Creating a Database Instance: Like BigQuery and MongoDB, it seems straightforward to create a database instance with its configuration settings. <br> <br>

(2) Connecting to Redis' Database Instance: I utilized Redis Insight to connect my Redis database instance to manage the data that will be uploaded. <br>

(3) Dataset Uploading or Insertion: I used a Python script in Visual Studio Code to insert the healthcare dataset into Redis, treating PatientID as the key.<br> </td>

</tr>
<tr>
<td>📌 Reflections on User-Interface and Usability </td>
<td> (1) GCP makes it easy for a beginner like me to write/run queries, explore the data, and manage tables. <br> <br>

(2) With the help of my weekly assignments with Oracle, I have recent exposure to SQL. This made it easier for me to start and run queries within the healthcare dataset. <br>

(3) BigQuery's speed in making analytical queries on large dataset is quite impressive. This observation is based on my experience with a previous assignment.<br> </td>

<td> (1) I find both the MongoDB Atlas web interface and MongoDB Compass visually appealing, particularly Compass. Similar to BigQuery, MongoDB Atlas (and Compass) provides the ability to manage newly created databases, collections (tables), and user access. Initially, I was confused, but after exploring the interface, I realized it was just unfamiliar to me. I prefer using Compass, which I downloaded on my laptop. <br> <br>

  (2) I need to get used to MongoDB's query language. Having been exposed to SQL queries, which I find easier compared to MongoDB, I got confused even after following my professor's video recording. However, I used the simplest query. I know with time and practice my querying skills will likely improve, which will be part of my learning journey.<br>

</td>

<td> (1) Similar to MongoDB Atlas and Compass, I find the Redis web interface and Redis Insight (downloaded on my laptop) visually appealing. However, I was confused while I was attempting to perform the Redis task. At some point while navigating, I almost gave up because I couldn't find what I was looking for, especially when I wanted to run simple queries to complete this assignment. Then, I realized that, like MongoDB, I am not quite familiar with Redis yet. I need more exposure and practice to get used to it. Also, I find that Redis is more complex, requiring more understanding and effort to get accustomed to the data and commands/languages to make this platform work for the datasets I will choose to import in the future compared to the other two platforms. This is probably just me. <br> <br>

(2) I noticed that in Redis, the default data type for keys is "string." For instance, after I uploaded the healthcare dataset and explored the data, "PatientID" were stored as a string by default for each patient information. This is my first time using Redis, and perhaps it is designed this way to make it more simplified in managing databases. For a beginner like me, it can be confusing, but as I mentioned previously in MongoDB, with time and practice my skills will likely improve. <br>

</td>
</tr>

</tr>
</tbody>
</table>

---
---

# ☞ _**My Final Thoughts:**_ 👩🏻‍💻
#### 📌 Having now gained experience working with BigQuery, MongoDB, and Redis, I recognize that each platform offers distinct advantages. However, I find myself leaning towards GCP's BigQuery. Its user-friendly or straightforward interface and impressive performance capabilities, makes it a standout choice for me. My experience in this current assignment and my previous assignments has strengthened my opinion that GCP is a powerful and efficient tool for handling and analyzing large datasets, making it ideal for beginners like myself. This is not to say that Azure, MongoDB, and Redis are not good options. I just find GCP pretty straightforward and a little less complicated.




