Q: I don't understand what `from .models import Comment` the "." before models mean. Is this similar to ../.. thing or something else?
A: The dot (`.`) before `models` in the import statement `from .models import Comment` indicates a relative import in Python. It means that the `models` module is located in the same package (directory) as the current module from which the import is being made.

---

Q: what is the Meta class in Django models? why we use it, where we should use it, is it necessary? 
For example: 
```python
    class Meta:
        ordering = ['created']
        indexes = [
            models.Index(fields=['created']),
        ]
```
explain in simple english?
A: The `Meta` class in Django models is a special inner class that provides metadata about the model. It is not necessary to use it, but it allows you to customize the behavior of your model in various ways.
By metadata we mean information about the model itself, such as how it should be ordered when queried, what database indexes should be created, and other options that affect the model's behavior. 
In the example you provided:
```python
    class Meta:
        ordering = ['created']
        indexes = [
            models.Index(fields=['created']),
        ]
```
- `ordering = ['created']`: This tells Django to order the results by the created field by default whenever you query this model. So, when you retrieve instances of this model, they will be sorted based on the `created` field in ascending order.
- `indexes = [ models.Index(fields=['created']), ]`: This specifies that a database index should be created on the `created` field. Indexes help speed up database queries that filter or sort by that field, improving performance.
In summary, the `Meta` class is used to define additional options for your Django model, allowing you to control how it behaves and interacts with the database.

---

Q: what is CSRF protection? 
A: 

---

Q: 
A:

---

Q: 
A:

---

Q: 
A:

---