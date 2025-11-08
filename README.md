MAKWANA MAULIK - Personal Portfolio & BlogThis repository contains the complete source code for my personal portfolio website and blog. It's a clean, modern, and fully responsive static site built with pure HTML, CSS, and JavaScript, designed to showcase my profile, professional summary, and personal thoughts.Preview(This is a placeholder. You can add a screenshot of your live website here!)PagesPortfolio (index.html): The main landing page featuring a profile card, an "About Me" (Namaste) section, and links.Blog (blog.html): A separate page that lists all blog posts. Clicking "Read More" reveals the full post content on the same page.FeaturesFully Responsive: Designed to look great on desktops, tablets, and mobile phones.Modern UI/UX: A sleek, dark-mode, "glassmorphism" aesthetic.Dynamic Blog Page: The blog list (blog.html) automatically uses JavaScript to find the main image from each full blog post and sets it as the thumbnail on the blog card.Interactive Modals: Clean, pop-up modals for "Contact" and "Share" that work across the entire site.Working Contact Form: The contact modal features an HTML form routed through formsubmit.co to send messages directly to your email.No Frameworks: Built with pure HTML5, CSS3, and modern JavaScript (ES6+) for fast performance and easy editing.Tech StackHTML5CSS3 (Custom Properties, Flexbox, CSS Grid)JavaScript (ES6+) (DOM Manipulation for Modals & Blog Navigation)Font Awesome (for icons)Google FontsFormSubmit.co (for the contact form backend)How to CustomizeThis site is designed to be easily customized.1. Update Personal Information (index.html)Profile: Open index.html and find the <section class="profile-card">. You can change your profile picture (src), name, quote, and social media href links here.About Me: Find the <section class="namaste-section"> to edit the "Namaste!" and paragraph text.Resume: In the <header>, change the resume link: href="path/to/your/resume.pdf".2. Update Header/Footer (index.html & blog.html)You must update the <header> and <footer> sections on both files to ensure navigation is consistent.Update your logo path.Update your email and social media links in the <footer>.3. Contact FormThe contact form in the modal will work automatically, but you should change the email address.Find the <form> inside the contact-modal HTML (it's in both index.html and blog.html).Change the action URL to use your own email:<form class="contact-form" action="[https://formsubmit.co/YOUR-EMAIL-HERE@gmail.com](https://formsubmit.co/YOUR-EMAIL-HERE@gmail.com)" method="POST">
Update the contact info (email, phone) listed in the modal's modal-contact-info section.4. How to Add a New Blog Post (blog.html)Adding a new post is a 3-step process. Let's say you want to add Post 7.Step 1: Create the Blog CardCopy an existing <article class="blog-card" ...> block. Change the data-post attribute to your new number.<!-- This is your new card for Post 7 -->
<article class="blog-card" data-post="7">
    <img src="[https://placehold.co/600x400/1a1a1a/ffffff?text=Loading](https://placehold.co/600x400/1a1a1a/ffffff?text=Loading)..." alt="Loading..." class="blog-card-image">
    <div class="blog-card-content">
        <h3>My New Blog Post Title</h3>
        <div class="blog-meta">
            <span><i class="far fa-calendar"></i> Nov 08, 2025</span>
            <span><i class="far fa-clock"></i> 4 min</span>
        </div>
        <p>A short summary of my new blog post goes here...</p>
        <a href="#" class="btn read-more-btn">Read More</a>
    </div>
</article>
Step 2: Create the Blog Post ContentFurther down in blog.html, copy an existing <section id="blog-post-X" ...> block. Change the id to match your new card's data-post number.<!-- This is your new hidden post content for Post 7 -->
<section id="blog-post-7" class="blog-post" style="display: none;">
    <div class="blog-post-header">
         <h1 class="blog-post-title">My New Blog Post Title</h1>
         <!-- Add your meta info here -->
    </div>
    
    <!-- 
      THIS IS THE IMPORTANT PART: 
      The JavaScript will automatically take this image 'src' 
      and put it on your card from Step 1.
    -->
    <img src="[https://placehold.co/800x400/your-image.jpg](https://placehold.co/800x400/your-image.jpg)" alt="My New Post Image" class="blog-post-image">
    
    <div class="blog-post-content">
        <!-- Add your full blog post content here -->
        <p>This is the full text of my new post...</p>
        <h2>A new heading</h2>
        <p>More text...</p>
    </div>

    <div class="blog-post-footer">
        <a href="#" class="back-to-blog"><i class="fas fa-arrow-left"></i> Back to Blog</a>
    </div>
</section>
Step 3: You're Done!The JavaScript (autoSetCardImages function) will automatically find the src from the blog-post-image in blog-post-7 and apply it to the blog-card-image on the card with data-post="7".LicenseThis project is licensed under the MIT License. See the LICENSE file for details.
