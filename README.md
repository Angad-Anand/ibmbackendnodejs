# ibmbackendnodejs

#Get all books - Using async callback function
function getBookList(){
return new Promise((resolve,reject)+>{
resolve(books);  })}
public_user.get('/',function(req,res){
getBookList().then((bk)=>res.send(JSON.stingify(bk,null,4)),(error)=>res.send("denied"));});"


#Search by ISBN - Using Promises
"function getFromISBN(isbn){
let book _ = books[isbn];
return new Promise((resolve,reject)=>{
if (book_){ resolve(book_); }
else{ reject("Unable to find book!");
public_users.get('/isbn/:isbn',function (req, res) {
const isbn = req.params.isbn;
getFromlSBN(isbn).then((bk)=>res.send(JSON.stringify(bk, null, 4)),(error) res.send(error) ) });"



#search By author
function getFromAuthor(author){
let Output=[];
return new Promise((resolve,reject)=>{
for(var isbn in books){
let book=books[isbn];
if(book.author===author){output.push(book);}}
resolve(output);})}
public_user.get('author/:author',function(req,res){
const author = req.parmas.author;
getFromAuthor(author).then(result=>res.send(JSON.stingify(result,null,4)));});
