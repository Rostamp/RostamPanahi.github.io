
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Rostam's Portfolio</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQYv2tcunTyErYFNgv4cTbIb2fGxCu-uaVidw&usqp=CAU'); /* Replace with your background image URL */
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    #circle {
      position: relative;
      width: 600px;
      height: 600px;
      background-color: lightgreen;
      border-radius: 50%;
      overflow: hidden;
    }

    .curved-section {
      position: absolute;
      width: 300px;
      height: 600px;
      border-radius: 50% 0 0 50%;
      background-color: white;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: center;
      padding: 20px;
      clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
      color: lightgreen;
    }

    .section {
      margin-bottom: 20px;
      cursor: pointer;
    }

    .section-image {
      width: 200px;
      height: 200px;
      object-fit: cover;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <div id="circle">
    <div class="curved-section">
      <div class="section" onclick="navigate('Homepage')">Homepage</div>
      <div class="section" onclick="navigate('Photography')">Photography</div>
      <div class="section" onclick="navigate('Ukulele')">Ukulele</div>
      <div class="section" onclick="navigate('Traveling')">Traveling</div>
      <!-- Add more sections here -->
    </div>

    <div class="homepage-content" id="homepage-content">
      <h1 id="homepage-heading">Hello, my name is Rostam.</h1>
      <p id="homepage-paragraph">
        Today I want to share 3 hobbies that I like to do when I have available.
        I enjoy making websites like this and this website is simple to go over so enjoy while you are at it.
      </p>
      <img class="section-image" src="https://media.istockphoto.com/id/1222703360/vector/outline-colorful-doodle-hobbies-set-stay-home-concept-top-table-and-video-games-painting.jpg?s=612x612&w=0&k=20&c=X7CCSAmyd0_ZNk-PTvGNsd863U1am4aAy5spTcE2e5s=" alt="Homepage Image">
    </div>

    <div class="photography-content" id="photography-content" style="display: none;">
      <h1 id="photography-heading">Photography</h1>
      <p id="photography-paragraph">
        Photography is a very enjoyable hobby for me. As a kid, I've seen my mom do photography and that inspired me.
        Nowadays when I travel, I like to take photos of nature and my adventures.
      </p>
      <img class="section-image" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR3FcebDQM-sMX4zOU831yXbrDTR65eBOMFqQ&usqp=CAU" alt="Photography Image">
    </div>

    <div class="ukulele-content" id="ukulele-content" style="display: none;">
      <h1 id="ukulele-heading">Ukulele</h1>
      <p id="ukulele-paragraph">
        Playing the Ukulele in my free time really helps with my mindset.
        I play it every day and have already learned many songs and notes.
        I recommend that you give it a try too!
      </p>
      <img class="section-image" src="https://cdn.thewirecutter.com/wp-content/media/2023/08/ukulele-2048px-9727.jpg?auto=webp&quality=75&width=1024" alt="Ukulele Image">
    </div>

    <div class="traveling-content" id="traveling-content" style="display: none;">
      <h1 id="traveling-heading">Traveling</h1>
      <p id="traveling-paragraph">
        Traveling is one of my most favorite hobbies. Of course, traveling takes time and planning, and that is not a problem for me.
        I love to plan things and visit places. Trying different cultures is a great experience for me. Like I mentioned, I like to do photography as I am traveling.
      </p>
      <img class="section-image" src="https://www.forbes.com/advisor/wp-content/uploads/2021/03/traveling-based-on-fare-deals.jpg" alt="Traveling Image">
    </div>
    <!-- Add more sections' content divs here -->

  </div>

  <script>
    let currentSection = 'Homepage'; // Initial section is set to Homepage

    function navigate(section) {
      document.getElementById(currentSection.toLowerCase() + '-content').style.display = 'none'; // Hide current section
      document.getElementById(section.toLowerCase() + '-content').style.display = 'block'; // Show selected section

      if (section === 'Photography') {
        document.getElementById('homepage-heading').innerText = 'Photography';
        document.getElementById('homepage-paragraph').innerText = 
          'Photography is a very enjoyable hobby for me. As a kid, I\'ve seen my mom do photography and that inspired me. Nowadays when I travel, I like to take photos of nature and my adventures.';
      } else if (section === 'Ukulele') {
        document.getElementById('homepage-heading').innerText = 'Ukulele';
        document.getElementById('homepage-paragraph').innerText = 
          'Playing the Ukulele in my free time really helps with my mindset. I play it every day and have already learned many songs and notes. I recommend that you give it a try too!';
      } else if (section === 'Traveling') {
        document.getElementById('homepage-heading').innerText = 'Traveling';
        document.getElementById('homepage-paragraph').innerText = 
          'Traveling is one of my most favorite hobbies. Of course, traveling takes time and planning, and that is not a problem for me. I love to plan things and visit places. Trying different cultures is a great experience for me. Like I mentioned, I like to do photography as I am traveling.';
      } else if (section === 'Homepage') {
        document.getElementById('homepage-heading').innerText = 'Hello, my name is Rostam.';
        document.getElementById('homepage-paragraph').innerText = 
          'Today I want to share 3 hobbies that I like to do when I have available. I enjoy making websites like this and this website is simple to go over so enjoy while you are at it.';
      }

      currentSection = section; // Update the current section
    }
  </script>
</body>
</html>
