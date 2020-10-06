# Django date input form

Use this to create a date input widget for a django form that uses a DateTimeField.
This particular for is a ModelForm


```python
from django import forms
from django.forms import ModelForm

from .models import Book

class DateInput(forms.DateInput):
    input_type = 'date'

class BookForm(ModelForm):
    model = Book
    fields = ['status', 'checked_out', 'due']
    widgets = {
        'checked_out': DateInput(),
        'due': DateInput(),
    }
    
```
