# Having Navigation displayed on all pages

![Navigation](images/Navigation.PNG)

I used code:

 ```{% include 'includes/navigation.html'%}```

I added the pre-existing naviagtion template using the code above to add the navigation to the sign up, sign in and reset password pages which didn't have the navigation displaying on these pages. 

# Addition of A Upskilling Tab and Dropdown on the Navigation

<!-- Image -->

Code:
```

          {% if user.is_authenticated %}
          <li class="nav-item dropdown">
            <a
              href="#"
              class="nav-link dropdown-toggle"
              id="frontPagesDropdown"
              aria-expanded="false"
              data-bs-toggle="dropdown"
            >
              Upskilling
              <span class="fas fa-angle-down nav-link-arrow ms-1"></span>
            </a>
            <div
              class="dropdown-menu px-0 py-2 p-lg-4"
              aria-labelledby="frontPagesDropdown"
            >
              <div class="row">
                <div class="col">
                  <ul class="list-style-none mb-4">
                    <li class="mb-2 menu-item">
                      <a class="menu-link" href="{% url 'dashboard' %}"
                        >Dashboard</a
                      >
                    </li>
                    <li class="mb-2 menu-item">
                      <a class="menu-link" href="{% url 'upskilling' %}"
                        >Skills</a
                      >
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </li>
          {% endif %}
```

When a user is signed into the website, Upskilling will be appearing on the navigation. It is a dropdwon which has the Dashboard which they can see their project preferences, allocation and their progress on their upskilling and it will have the Upskilling page which will have links to Django, Front End Design, Python etc skills that they can redirect to.