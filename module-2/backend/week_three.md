## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
* rails new appname -d= "database"

2. What do Models generally inherit from in rails?
* ActiveRecord

3. What do Controllers generally inherit from in a rails project?
* ActionController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
* create it in routes (resources :horses). Then if you wanted to see one horse it would be the horse_path(horse) path helper.

5. What rake task is useful when looking at routes, and what information does it give you?
* rake routes, gives you the list of routes with their verbs and prefixes.

6. What is an example of a route helper? When would you use them?
* something_path(something). You use this instead of writing out /something/:id.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
* the _url will give you the whole url to the path while _path just gives you the uri

8. What are strong params and why are they necessary?
* They filter what params can be passed in. When you only certain attributes passed in by a user.

9. What role does `form_for` play in helping us create our forms?
* form_for give us a form that a user can fill out and pass in information with a put request. It also can assign paths based on what instance variable you pass it.

10. How does `form_for` know where to submit the user's input?
* Based on the instance variable/variables you pass to it.

11. Create a form using a `form_for` helper to create a new `Horse`.
* <%=form_for @horses do |f| %>
    <%= f.label :name %>
    <%= f.text_field :name %>

    <%= f.label :breed %>
    <%= f.text_field :breed %>

    <%= f.submit %>
    <%end%>

12. Why do we want to validate our models?
* So they have the same attributes every time we save it to the database. Otherwise it could be challenging to look it up\ afterwards.

13. What are the steps of the DNS lookup?
* First it checks the operating system, then it checks the .com servers, then it goes to a name server, then it goes to the server where it is hosted, then back down the chain to your browser.


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
class Horse

def self.prance
  prance
end

def move
  prance
end
end

Horse.new.move
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
* furniture[:table][:height]
* furniture[:purchased]


16. What is inheritance?
* It allows your class to reuse code and  call methods from a class that it is inheriting from with out defining them within the class.


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
