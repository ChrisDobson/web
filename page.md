# My Week 7 Project: APIs, URLs, and Sacred Timelines

<img
      src="Me.jpg"
      alt="A man stands on a wall next to the River Thames. The Sun is shining brightly and the Shard, Britain's tallest building, rises in the distance."
      width="500"
      height="600" />

It’s week 7 of my [Software Development in JavaScript - Skills Bootcamp](https://northcoders.com/our-courses/skills-bootcamp-in-software-development) with Northcoders. It’s an unusual week, because rather than working in pairs, this week I will be working independently on a project to consolidate what I have learned during the backend block of the course.

‘Backend’ refers to all the coding that goes on behind-the-scenes, as opposed to frontend, which a user sees when they visit a website or app. The aim of this week’s project is to create the components for a message board, a bit like Reddit, in which users can post articles and other users can interact with these posts. Conveniently, the nice tutors at Northcoders have already created a database, which contains all the articles, comments and users that I will need to populate my app.

At this point, I need to introduce a technical term: Application Programming Interface (API), which I will use to create my website. You know how all websites have a URL (Uniform Resource Locator), i.e. the address by which you access them? Imagine that [/api](https://my-nc-news-2zd4.onrender.com/api) is the URL for my website. (I’m simplifying a bit here.) My job is to create endpoints for my URL, e.g. [/api/articles](https://my-nc-news-2zd4.onrender.com/api/articles), which will navigate a user to a page containing all of the articles. Once I have created an endpoint, I then need to write several tests to check that it works. Still with me?

For example, [/api/articles/1](https://my-nc-news-2zd4.onrender.com/api/articles/1) takes you to a page containing only the article with an ID of 1. However, if a user types in an article ID that does not exist in the database, such as [/api/articles/999](https://my-nc-news-2zd4.onrender.com/api/articles/999), they will receive a 404 error and this message: “Article ID not found”. Once I am satisfied that an endpoint works as expected, I can upload it to GitHub, which is a platform that developers use to save their code.

Things are about to get complicated. Have you seen the Marvel series *Loki*? In season 1, Loki gets into trouble with the Time Variance Authority (TVA). This organisation is in charge of the ‘Sacred Timeline’. If a person goes back in time and changes things, a branch of the Sacred Timeline is created. For example, in the Sacred Timeline, Loki died, but then a branch was created in which he still lives. On GitHub, your code has a main branch, which is a bit like the Sacred Timeline. Every time I create a new endpoint, I also make a new branch. Once I am satisfied, I can merge the changes I have made into the main branch.

This sounds straightforward enough, but difficulties can arise if you lose track of which branch you are on. For instance, on day 2 of project week, I received a merge conflict. This meant that I was unable to merge changes into my main branch until I resolved a discrepancy between the two branches. This was frustrating, because I had made several changes and it was not immediately apparent what was causing the issue. Once I had finally sorted things out, I resolved not to make this mistake again! Using good old pen and paper, I created a 10-point checklist of each step I needed to take when creating and saving a new branch.

On day 4, it was time for my website to go live! In that morning’s lecture, I learned that there are two main ways to host a website: on a physical server (expensive!) or on a cloud server. For this project, I used Render (a cloud server) to host my website, allowing anyone in the world to access it using the URL endpoints I had created. It was gratifying to see my website ‘in the flesh’, as it were, even though at this stage it was pretty bare bones. Later, during the frontend block of the course, I will create the visual side of things to aid user experience.

In addition to endpoints, I created queries that a user can apply to refine their search. Let’s break down this (abridged) URL: [/api/articles?topic=coding&limit=4&sort_by=author&order=asc](https://my-nc-news-2zd4.onrender.com/api/articles?topic=coding&limit=4&sort_by=author&order=asc).

- [/api/articles](https://my-nc-news-2zd4.onrender.com/api/articles) takes users to a page containing all of the articles in the database. The total_count of articles is 37.
- [?topic=coding](https://my-nc-news-2zd4.onrender.com/api/articles?topic=coding) returns only articles with a topic of coding. Now the total_count is 12.
- [&limit=4](https://my-nc-news-2zd4.onrender.com/api/articles?topic=coding&limit=4) returns only the first four articles, but total_count remains 12.
- [&sort_by=author](https://my-nc-news-2zd4.onrender.com/api/articles?topic=coding&limit=4&sort_by=author) sorts the articles alphabetically by author, in descending order by default.
- [&order=asc](https://my-nc-news-2zd4.onrender.com/api/articles?topic=coding&limit=4&sort_by=author&order=asc) changes the order to ascending.

A user can also add another query, &p=1, which ensures that only the first four results are returned. (Remember that the page limit has been set to 4 in this example.) If p was set to 2, it would skip the first four results and return results 5 – 8. Likewise, p=3 returns results 9 – 12, and since there are only 12 results in total, any further page requests will result in an error. (Unless topic=coding is removed from the query.) The order of the queries is unimportant, but the question mark at the beginning of the query string is essential.

In total, project week consisted of 23 tasks. At the beginning, this felt quite daunting and I was worried that I would not have enough time to finish everything. My approach was to take stock of the progress that I had made, again with the aid of an old-fashioned notebook. I made a list of each task and I ticked them off as I completed them. I also kept track of the number of tests for each endpoint.

I had created over 20 new files in my repository (that’s the name for the collection of code which is stored on GitHub), so on day 5 I dedicated a lot of time to re-organising these files, so that a different developer could easily understand it. I encourage you to take a look for yourself by going to [GitHub](https://github.com/ChrisDobson/my-nc-news). You can also connect with me on [LinkedIn](https://www.linkedin.com/in/christopher-d-572004256/).

**View my CV here: [Christopher Dobson's CV](https://chrisdobson.github.io/web/)**
