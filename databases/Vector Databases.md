**1️⃣ Vector Databases (වෙක්ටර් ඩේටාබේස්)**


👉 AI systems වලට අත්‍යවශ්‍ය Database type එකක්
🔹 Vector Database කියන්නේ මොනවාද?
Data (text, image, audio වගේ දේවල්)
👉 numbers (vectors) ලෙස store කරන database එකක්.

මේ vectors වලින් data එකේ meaning (අර්ථය / context) represent වෙනවා.

🔹 සාමාන්‍ය Database vs Vector Database

Normal Database (SQL / NoSQL):

“apple” කියන word එක search කලොත්
👉 exact match තියෙන records විතරයි.

Vector Database:

“apple” search කලොත්
👉 “fruit”, “red fruit”, “healthy food” වගේ
අර්ථයෙන් සමාන දේවල්ත් හොයාගන්න පුළුවන්.

👉 මේකට කියන්නේ Semantic Search.

🔹 AI වලට Vector DB වැදගත් ඇයි?

Chatbots (ChatGPT වගේ)
Recommendation systems
Document search (PDF, notes)
Image & voice recognition

AI model එකට: “මේකට සම්බන්ධ data මොනවාද?” කියලා meaning-wise හොයාගන්න පුළුවන්.

🔹 Example (simple)

ඔයා AI chatbot එකක් හදනවා කියලා හිතන්න.

User:

“Invoice generate කරන එක explain කරන්න”

Vector DB එක:

Exact words නැති උනත්

similar meaning තියෙන documents හොයාගෙන

AI එකට context එක supply කරනවා.
👉 ඒකෙන් AI answer එක smart & accurate වෙනවා.

####################################################################################


*   more about vector databases the conecept name is convert normal text into vector called -- embedding --
*   An AI model called an embedding model do above converting process
Below represent the process step by step :
         Normal Text 
              |
        Embedding model(AI)
              |
         vector (numbers)
              |
        Stored in vector database 

* in the vector databse it recognise when numbers(vectors) are very close - meaning is similar 






