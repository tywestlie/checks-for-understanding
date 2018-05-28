## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
* Cookie is a small file that is held in the clients browser

2. What’s the difference between a session and a cookie?
* A Session is stored in the database and a cookie is only in the users browser.

3. What’s a flash and when do you want to use flashes?
* It's a pop up HTML message, whenever a user does something.

4. Why do people say “HTTP is stateless”?
* It doesn't 'remember' any information passed through the protocol.

5. What’s authentication? Explain.
* Authentication is creating or verifying a users credentials in order to identify them.

6. What’s the difference between authentication and authorization?
* Authentication gets you into the application, authorization is what you are permitted to do while in the application.

7. What’s a before filter?
*  It sets a method in the controller before an action takes place. It can be used to check user status before continuing with an action.

8. How do we keep track of a user once they’ve logged in?
* Using session data

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
* Namespacing a resource is used for requiring a level of authorization to access parts of that resource.
* When a resource is dependent on another resource.
* Namespacing is part of authorization and nesting is more about creating routes when creating resouces in the database.

10. At a high level, what tools can you use to implement authorization? How would you use them?
* Enums. You assign the role of users at the model level.

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
* It allows you to assign roles to each user that is created. It needs to be an integer. At the model level.

12. What are some strategies you can use to keep your views DRY?
* Keep all of the active record calls out of you view. Keeping any ruby logic out of your view other than authorization logic.


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[{holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"] }, {holiday: {name: "Halloween", supplies: ["Candy", "Costume"] }, {holiday: {name: "Hanukkah", supplies: ["Menorah"] } ]
```  
given.map do | holiday|
  holiday.values
  end.sort

  (I wanted to test this out but I couldn't get it to work in pry)


14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
*  def clean(num)
      num.to_i
    end


### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel comfortable with the content presented this week
