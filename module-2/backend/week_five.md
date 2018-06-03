### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
* You set up the message in the controller action where you want the message to occur. If you wanted a flash message to pop up when you create in the DB you would write something like
```
if item.save
  flash[:success] = "You successfully created an item!"
end
```
2. Where is cart information/temporary information usually stored?
* In the session

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
*  If a visitor to the site doesn't want to create an account, but we want them to fill their cart with items.

4. What is the purpose of the asset pipeline?
* To reduce the amount of files we are sending through a request and speed up load times.

5. Why do we precompile our assets?
* To prepare the files that are being sent. Specific examples would be merging CSS and JS into one file respectively.

6. What do each of the following tags do?

`<%= stylesheet_link_tag "application" %>`
* It loads a precompiled application.css that contains all of the CSS in our application
`<%= javascript_include_tag "application" %>`
* It loads a precompiled application.js that contains all of the JS in our application
`<%= image_tag "rails.png" %>`
* It loads a precompiled file that contains all of our image files.

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
* It's the first thing people will go to when they are having trouble setting up, using and debugging your program. Some elements that make it great would be a lot of details and specific code examples of how to use the program.

8. What are the top four accessibility issues that we as developers should be aware of?
* I don't remember this lesson but I'll guess off my internet searches.
  -Navigation
  -Links
  -Images
  -Site structure

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
* its a callback. You could put this in the controller or at the model level.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
* scope :active, -> {where(active: true)}

11. What is the difference between a scope and a class method?
* A scope can contain class methods inside of it. A class method is specific to a class.


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
  * given[:cart]["48"] = 4
  12b. How would you increase the quantity of item 29?  
  * given[:cart]["29"] += 1
  12c. How would you find out how many items your user is thinking about purchasing?   
  * give[:cart].value.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
* Polymorphism in OOP is when one object can interact different datatypes.
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
* given.gsub(")",".").gsub("-",".")


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week
