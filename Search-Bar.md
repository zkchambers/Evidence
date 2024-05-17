# Addition of Search Bar to Navigation

Code:

``` <form class="d-flex align-items-center" method=POST action="{% url 'pages/search-results'%}">
          {% csrf_token %}
          <input class="form-control mr-sm-2" type="search" style="margin-left: 50px;" placeholder="Search..." aria-label="Search" name="searched">
          <button class="btn btn-outline-gray-100 me-md-3 px-4" style="margin-left: 10px;" type="submit">Search</button>
        </form>
```
Worked with Nick on the search bar, I did the front end side and incorportated the search bar into the navigation and he worked on the backend side and made sure that the search bar was functional.

