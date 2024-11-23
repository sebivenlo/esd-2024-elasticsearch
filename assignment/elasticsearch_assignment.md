```json
PUT /books
{
  "mappings": {
    "properties": {
      "title": { "type": "text" },
      "author": { "type": "text" },
      "publication_date": { "type": "date" },
      "isbn": { "type": "keyword" },
      "genre": { "type": "keyword" },
      "summary": { "type": "text" }
    }
  }
}
```
```json
DELETE /books
```
```json
GET /books
```

```json
POST /books/_bulk
{ "index": {} }
{ "title": "The Silent Patient", "author": "Alex Michaelides", "publication_date": "2019-02-05", "isbn": "9781250301697", "genre": "Thriller", "summary": "A psychological thriller about a woman who shoots her husband and then stops speaking." }
{ "index": {} }
{ "title": "Where the Crawdads Sing", "author": "Delia Owens", "publication_date": "2018-08-14", "isbn": "9780735219090", "genre": "Fiction", "summary": "A coming-of-age story and a murder mystery set in the marshes of North Carolina." }
{ "index": {} }
{ "title": "Educated", "author": "Tara Westover", "publication_date": "2018-02-20", "isbn": "9780399590504", "genre": "Memoir", "summary": "A memoir about a woman who grows up in a strict and abusive household in rural Idaho but eventually escapes to learn about the wider world through education." }
{ "index": {} }
{ "title": "Becoming", "author": "Michelle Obama", "publication_date": "2018-11-13", "isbn": "9781524763138", "genre": "Biography", "summary": "The former First Lady of the United States recounts her life story, from her childhood in Chicago to her years in the White House." }
{ "index": {} }
{ "title": "The Testaments", "author": "Margaret Atwood", "publication_date": "2019-09-10", "isbn": "9780385543781", "genre": "Dystopian", "summary": "A sequel to 'The Handmaid's Tale' that continues the story of Gilead and its oppressive regime." }
{ "index": {} }
{ "title": "Normal People", "author": "Sally Rooney", "publication_date": "2018-08-28", "isbn": "9781984822178", "genre": "Romance", "summary": "A novel about the complex relationship between two young people from a small town in Ireland." }
{ "index": {} }
{ "title": "The Night Circus", "author": "Erin Morgenstern", "publication_date": "2011-09-13", "isbn": "9780385534635", "genre": "Fantasy", "summary": "A magical competition between two young illusionists that takes place within a mysterious traveling circus." }
{ "index": {} }
{ "title": "The Goldfinch", "author": "Donna Tartt", "publication_date": "2013-10-22", "isbn": "9780316055437", "genre": "Literary Fiction", "summary": "A young boy in New York City miraculously survives an accident that takes his mother's life and is taken in by a wealthy family." }
{ "index": {} }
{ "title": "Little Fires Everywhere", "author": "Celeste Ng", "publication_date": "2017-09-12", "isbn": "9780735224292", "genre": "Fiction", "summary": "A story about the intertwined fates of the picture-perfect Richardson family and the enigmatic mother and daughter who upend their lives." }
{ "index": {} }
{ "title": "The Alchemist", "author": "Paulo Coelho", "publication_date": "1988-04-15", "isbn": "9780061122415", "genre": "Adventure", "summary": "A young shepherd named Santiago travels from Spain to Egypt in search of treasure and discovers his personal legend." }
{ "index": {} }
{ "title": "The Road", "author": "Cormac McCarthy", "publication_date": "2006-09-26", "isbn": "9780307265432", "genre": "Post-Apocalyptic", "summary": "A father and son journey through a desolate, post-apocalyptic landscape, struggling to survive." }
{ "index": {} }
{ "title": "The Girl on the Train", "author": "Paula Hawkins", "publication_date": "2015-01-13", "isbn": "9781594634024", "genre": "Thriller", "summary": "A psychological thriller about a woman who becomes entangled in a missing persons investigation." }
{ "index": {} }
{ "title": "The Book Thief", "author": "Markus Zusak", "publication_date": "2005-03-14", "isbn": "9780375842207", "genre": "Historical Fiction", "summary": "A young girl in Nazi Germany finds solace by stealing books and sharing them with others." }
{ "index": {} }
{ "title": "Gone Girl", "author": "Gillian Flynn", "publication_date": "2012-06-05", "isbn": "9780307588364", "genre": "Mystery", "summary": "A thriller about a man whose wife goes missing, and the media frenzy that follows." }
{ "index": {} }
{ "title": "The Hobbit", "author": "J.R.R. Tolkien", "publication_date": "1937-09-21", "isbn": "9780547928227", "genre": "Fantasy", "summary": "Bilbo Baggins embarks on an unexpected journey to reclaim a stolen treasure from a dragon." }
{ "index": {} }
{ "title": "Pride and Prejudice", "author": "Jane Austen", "publication_date": "1813-01-28", "isbn": "9781503290563", "genre": "Classic", "summary": "A romantic novel that explores the manners and matrimonial machinations among the British gentry of the early 19th century." }
{ "index": {} }
{ "title": "The Da Vinci Code", "author": "Dan Brown", "publication_date": "2003-03-18", "isbn": "9780385504201", "genre": "Thriller", "summary": "A symbologist and a cryptologist uncover a secret that could shake the foundations of Christianity." }
{ "index": {} }
{ "title": "The Shining", "author": "Stephen King", "publication_date": "1977-01-28", "isbn": "9780385121675", "genre": "Horror", "summary": "A family heads to an isolated hotel for the winter where an evil presence influences the father into violence." }
{ "index": {} }
{ "title": "The Catch-22", "author": "Joseph Heller", "publication_date": "1961-11-10", "isbn": "9781451626650", "genre": "Satire", "summary": "A satirical novel about the absurdities of war and bureaucracy, centered on a World War II bomber squadron." }
{ "index": {} }
{ "title": "The Kite Runner", "author": "Khaled Hosseini", "publication_date": "2003-05-29", "isbn": "9781594631931", "genre": "Fiction", "summary": "A story of friendship and redemption set against the backdrop of a changing Afghanistan." }
{ "index": {} }
{ "title": "Brave New World", "author": "Aldous Huxley", "publication_date": "1932-08-18", "isbn": "9780060850524", "genre": "Dystopian", "summary": "A novel set in a futuristic world where society is controlled through technology and conditioning." }
{ "index": {} }
{ "title": "The Handmaid's Tale", "author": "Margaret Atwood", "publication_date": "1985-09-01", "isbn": "9780385490818", "genre": "Dystopian", "summary": "A story about a woman living in a totalitarian society where women are subjugated and used for reproduction." }
{ "index": {} }
{ "title": "Moby-Dick", "author": "Herman Melville", "publication_date": "1851-10-18", "isbn": "9781503280786", "genre": "Adventure", "summary": "The narrative of Captain Ahab's obsessive quest to kill the white whale, Moby-Dick." }
{ "index": {} }
{ "title": "War and Peace", "author": "Leo Tolstoy", "publication_date": "1869-01-01", "isbn": "9780199232765", "genre": "Historical Fiction", "summary": "A novel that intertwines the lives of several families against the backdrop of the Napoleonic Wars." }
{ "index": {} }
{ "title": "Crime and Punishment", "author": "Fyodor Dostoevsky", "publication_date": "1866-01-01", "isbn": "9780140449136", "genre": "Psychological Fiction", "summary": "A psychological drama about a young man who commits a crime and struggles with guilt and redemption." }
{ "index": {} }
{ "title": "The Catcher in the Rye", "author": "J.D. Salinger", "publication_date": "1951-07-16", "isbn": "9780316769488", "genre": "Fiction", "summary": "A story about teenage rebellion and angst, narrated by the iconic Holden Caulfield." }
{ "index": {} }
{ "title": "To Kill a Mockingbird", "author": "Harper Lee", "publication_date": "1960-07-11", "isbn": "9780061120084", "genre": "Fiction", "summary": "A novel about the serious issues of rape and racial inequality, told through the eyes of a young girl in the Deep South." }
{ "index": {} }
{ "title": "1984", "author": "George Orwell", "publication_date": "1949-06-08", "isbn": "9780451524935", "genre": "Dystopian", "summary": "A chilling depiction of a totalitarian regime and the control it exerts over its citizens." }
{ "index": {} }
{ "title": "The Great Gatsby", "author": "F. Scott Fitzgerald", "publication_date": "1925-04-10", "isbn": "9780743273565", "genre": "Classic", "summary": "A story of the mysteriously wealthy Jay Gatsby and his love for the beautiful Daisy Buchanan, set in the Jazz Age." }
{ "index": {} }
{ "title": "A Brief History of Time", "author": "Stephen Hawking", "publication_date": "1988-03-01", "isbn": "9780553380163", "genre": "Science", "summary": "An exploration of the universe's biggest questions, from the Big Bang to black holes." }
```