# Changes to Skills Pages Django, Python and Front End Design

<!-- Image -->

```
{% extends 'pages/upskilling/skill_base.html' %} 
{% load static %}


{% block skill_content %}


<div class="container">
  <div id="sections" class="my-5">
    <section class="section card mb-3 p-3">
      <h2 class="card-title">Structure</h2>
      <p class="card-text">Django follows the MVT architecture. MVT stands for Model-View-Template. In an MVT architecture, there are three parts to this architecture: Model: The model provides a logical data structure to the application and maintains data with the help of a database. Reference: <a href="https://www.naukri.com/code360/library/project-structure-in-django">Code360 Project Structure in Django</a></p>
    </section>

    <section class="section card mb-3 p-3" style="display: none">
      <h2 class="card-title">Syntax</h2>
      <p class="card-text">Django’s template language is designed to strike a balance between power and ease. It’s designed to feel comfortable to those used to working with HTML. Reference: <a href="https://docs.djangoproject.com/en/5.0/ref/templates/language/">Django Offical Documentation</a></p>
    </section>

    <!-- More sections... -->
  </div>

  <div class="d-flex justify-content-between mb-4">
    <button id="back-button" class="btn btn-secondary" style="display: none">Back</button>
    <button id="next-button" class="btn btn-primary">Next</button>
    <button id="finishButton" class="btn btn-warning" style="display: none">Finish</button>
  </div>
```
Added cards about the structure and syntax of the skill which you can go through the cards using the next or back button.

<!-- Image-->
```
<script>
    window.progressId = "{{ progress_id }}";
    window.csrfToken = "{{ csrf_token }}";
       // Function to handle button visibility for cards so that the finish button is invisible on the first card and the next button is invisible on the second card
       function toggleButtons(currentIndex, totalCards) {
        if (currentIndex === 0) {
            // If it's the first card, hide the back button
            document.getElementById("back-button").style.display = "none";
        } else {
            // Otherwise, show the back button
            document.getElementById("back-button").style.display = "block";
        }

        if (currentIndex === totalCards - 1) {
            // If it's the last card, hide the next button and show the finish button
            document.getElementById("next-button").style.display = "none";
            document.getElementById("finishButton").style.display = "block";
        } else {
            // Otherwise, show the next button and hide the finish button
            document.getElementById("next-button").style.display = "block";
            document.getElementById("finishButton").style.display = "none";
        }
    }

    var currentIndex = 0; // Update this value based on user navigation
    var totalCards = document.querySelectorAll("#sections .section").length;

    //Toggle of Button Visibility 
    toggleButtons(currentIndex, totalCards);

    // Event listener for the back button click
    document.getElementById("back-button").addEventListener("click", function() {
        currentIndex--;
        toggleButtons(currentIndex, totalCards); // Update button visibility
    });

    // Event listener for the next button click
    document.getElementById("next-button").addEventListener("click", function() {
        currentIndex++;
        toggleButtons(currentIndex, totalCards); // Update button visibility
    });
</script>
</script>

<script src="{% static 'skill_navigation.js' %}"></script>

{% endblock %}
```
I developed a script to control the visibility of "Next" and "Finish" button under the cards. The script ensures that the "Finish" button is hidden on the first card and the "Next" button is hidden on the last card.
