## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.

** Get: Sends a request to a server for information that can be read by the browser on the client device.
** Post: Sends a request to create information on a server.
** Put: Sends a request to update information on a server.
** Patch: Sends a request to modify specific information on a server.
** Delete: Sends a request to delete information on a server.
2. What is Sinatra?
** Sinatra is a ruby framework used to create web applications.
4. What is MVC?
** MVC stands for Model, View and Controller. The model is the relationship between objects and the database. The View is the presentation of data. The Controller directs the traffic of data between the model and the view.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
** So other developers can read the code we create.
6. What types of variables are accessible in our view templates without explicitly passing them?
** instance variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    @name = 'Mr. Ed'
    erb :index
  end
  ```
  
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
9. What's the purpose of ERB?
** Translate ruby code into into HTML.
10. Why do I need a development AND test database?
** So you can follow the SEAT testing convention. You create new data each time you test. You want to have the same data in your development database regardless of your tests.
11. What is CRUD and why is it important?
** Create, Read, Update, Delete. It is how you interact with a database.
12. What does HTTP stand for?
** Hypertext transfer protocol.
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
** <%ruby.code%> and <%= ruby.code%>. The first one runs the ruby code behind the scenes and the second transforms the return into HTML.
14. What's an ORM?
** Object Relational Mapper
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
** Active Record
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
** get /items - Shows all of the available items.
** post /items/new - Creates a new item.
** get /item/:id - shows one item.
** put /item/:id - updates a specific item.
** patch /item/:id - updates a specific aspect of an item.
** delete /item/:id - deletes item based on the id.
17. What's a migration?
** it is an action that creates or updates a database.
18. When you create a migration, does it automatically modify your database?
** Yes
19. How does a model relate to a database?
** The model is what reaches into the database to retrieve information. It also manipulates that data so the controller can send it specially tailored to the view.
20. What is the difference between `#new` and `#create`?
** New creates a new database table and create creates a new migration.

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
** create a migration with the attributes id, title and description and seed the database with the CSV file.
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
activities[:hiking][:supplies] = 'granola bar'
```
How would I add 'granola bar' to things you should have when hiking?

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
** Encapsulation: Separating responsibilities and hiding data from public methods.
** Abstraction: Knowing something at a high-level, not showing all of the internal parts required for some action.
** Inheritance: You can gain behavior from another piece of code without duplicating the code.
** Polymorphism: Methods can take in many arguments and behave accordingly.

### Self Assessment:
Choose One: (erase the others)

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
