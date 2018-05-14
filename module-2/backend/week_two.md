## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
* It an object relational mapper. It the model in MVC and gives you methods that you can use to interact with the database.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
* .find, .all, .find_by() .create(). Because you're inheriting ActiveRecord::Base.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
* Team.find(4).name
* team = Team.find(4)
* team_owner = team.owner_id

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

* team_owner = Team.find_by(owner_id: 4)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
* ```   
  A teacher will has_many students and a student belongs_to a teacher

  create_table "students", force: :cascade do |t|
    t.string "name"
    t.bigint "teacher_id"
    t.index ["teacher_id"], name: "index_students_on_teacher_id"
  end

  create_table "teachers", force: :cascade do |t|
    t.string "name"
  end

  ```
6. Define foreign key, primary key, and schema.
* A foreign key is an ID on a table that links the data to another table. A primary key is the unique ID associated to each resource on a table. The schema is the blueprints for a database.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
* A foreign key on one table is going to be the primary key on another table.
8. What are the parts of an HTTP response?
* A status code, Headers, and a body message.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
* created_at and updated_at.
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
* A school has_many teachers.
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
* ```
create_table "teachers", force: :cascade do |t|
  t.string "name"
  t.bigint "school_id"
  t.index ["school_id"], name: "index_teachers_on_school_id"
end

create_table "schools", force: :cascade do |t|
  t.string "name"
end
  ```
6. Give an example of when you might want to store information besides ids on a join table.
* If you were doing a student to classes join table. Each has_many but each one has a Grade(A,B,C,D,F) associated to it.
7. Describe and diagram the relationship between patients and doctors.
* ```
create_table "patients", force: :cascade do |t|
  t.string "name"
  t.bigint "doctor_id"
  t.index ["doctor_id"], name: "index_patients_on__id"
end

create_table "doctors", force: :cascade do |t|
  t.string "name"
end
  ```

8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel comfortable with the content presented this week
