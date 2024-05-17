# Addition of Search Bar to Navigation

Code:

``` <form class="d-flex align-items-center" method=POST action="{% url 'pages/search-results'%}">
          {% csrf_token %}
          <input class="form-control mr-sm-2" type="search" style="margin-left: 50px;" placeholder="Search..." aria-label="Search" name="searched">
          <button class="btn btn-outline-gray-100 me-md-3 px-4" style="margin-left: 10px;" type="submit">Search</button>
        </form>
```
Collaborated with Nick on implementing the search bar. I focused on the front-end aspect, incorporating the search bar into the navigation menu. Meanwhile, Nick handled the back-end development, ensuring the search bar was fully functional.

