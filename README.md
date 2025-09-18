# MentalHealthStudentPortal



## 1. Problem
The problem that our project aims to address is the lack of mental health support resources in schools. As reported by Delray Beach Psychiatrists, a significant percentage of schools do not have counselors, school psychologists, or social workers on staff to provide support to students who may be experiencing mental health challenges. With the increasing number of mental health issues among students, it is essential to provide a system that can help schools manage and track the mental health of their students effectively. Many schools do not have a system to accomplish that in place to address these concerns in a timely manner. 

## 2. Motivation
This lack of resources can leave students without access to the care they need, potentially exacerbating their mental health issues and impacting their academic performance. Public institutions can utilize our system to collect mental health surveys and gain insights into the overall health of the student body. This information can help schools identify and prioritize the most pressing issues and allocate resources effectively.

## 3. Features
The system being designed allows students to register and take mental health assessments,
after which they will be assigned to a mental health volunteer for further support. The system allows students to track their visits and compare past surveys, and volunteers to create records and provide direct assistance. The data structures are searchable and filterable, allowing for easy input and retrieval of patient data. However, the system's goal is not to provide diagnoses but rather connect students to
necessary resources and check self-progress, as diagnoses require trained and empathetic professionals:

1. Student Side:
    - **Search** - Students will be able to view their information (including name, email, phone number, address, school name, school year, date of birth) using their name, dob, address, phone, email, or a uniquely assigned ID.
  
   - **Insert** - When a new student accesses the website, they can create a record inside the portal if they have never provided information in the system.

   - **Delete** - A student can delete their information when they log into the portal. This is done so that all the records attached to that student are removed.

   - **Modify** - If a student wants to update their records in a while, they can do so by logging into the portal. They may also submit surveys on their current mental state that will update the student records on the urgency they need assistance.

2. Staff/Volunteer Side:
  
   - **Search** - Employees will be able to view information using their unique staff ID. They can also fetch a particular student record by using the student UD.

   - **Insert** - When a new student comes in, an employee can manually enter information and register on behalf of the student.

   - **Delete** - An Employee can delete a student’s information when they provide a student's ID. An employee won’t be able to delete their records (by design and to reduce complexity).

   - **Modify** - An Employee may also update students’ records by providing their uniquely assigned student ID.
 
## 4. Data
We are using randomly generated data based on real dataset examples to make up for the 100,000+ unique tuples. The fields in our data set will include: {Student ID: String, Email: String, Name: String, Phone Number: Integer, Age Group: String, Race Ethnicity: String, Sex: String, DOB: Date, Address: String, Survey Submitted: Date-Time (automatic on insertion), Area of Interest: String, Institution Name: String, Academic Level: String, GPA: String, Marital Status: String, Housing Condition: String, Family Size: String, Mother’s Education: String, Quantity of Visits: Integer, Employee ID: String (won’t be viewable on student’s side), Employee Name: String, Happiness Score: Float, Are you feeling depressed? - Have you ever been diagnosed with depression or anxiety before?: Boolean 

## 5. Tools/Languages/APIs/Libraries used
We used the Python programming language and the Flask web framework to develop the system. We implemented Hash Tables and B-trees to efficiently store and manage a fictional dataset.In addition to these, we used utility python packages such as pandas, time, datetime, csv, random, and data table and standard data containers such as data frames, dictionaries, lists and tuples. We are also using GitHub and Trello for checkpoints and project tracking. We also used R to create the fake data set. In R, we used the following libraries to assist generating the data: randomNames, openxlsx, data.table, tidyverse, generator, and leaflet. Lastly, we used a site called FakeNameGenerator to generate fake, yet believable, house addresses in the FL, USA.

## 6. Algorithms implemented
Hash tables and B-trees are both data structures that can be used to store information about students and their records. In a hash table, a built-in list data structure is used to implement separate chaining. This prevents collisions, which occur when two different keys are hashed to the same slot in the hash table. The slots of the hash table contain lists of key-value pairs, while B-trees contain dictionaries of key-value pairs. When a collision occurs, a new key-value pair is simply added to the list or node at the corresponding slot. Each slot in a hash table can contain multiple key-value pairs, and so collisions can be resolved by using a list data structure for separate chaining. For a B-tree, information is simply added in the correct position.
The advantage of using a list data structure for separate chaining is that it is simple to implement and can be used with any hashing function. Additionally, it allows for a high degree of flexibility, as the size of the lists can be adjusted based on the number of collisions that occur. On the other hand, using a dictionary to store node information inside the B-tree allows B-trees to be scaled to very large sizes. For example, if the student uses the mental health services again in the future, their information gets added to their respective node's dictionary. 
