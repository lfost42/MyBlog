# Project
A blog built with ASP.NET Core MVC with Class Library. Uses Entity Framework Core and deployed with a PostgreSQL database. Implements role and identity-based access, custom routing, front-end layouts, and accessing CRUD functions through modals. 

My code-centric blog articles and tutorials - http://lfost42-blog.herokuapp.com/

Summary Info

![My App](./app.png)

## WALKTHROUGH
A blog that allows the owner to post articles upon being authenticated via login. Users may leave comments after registering and being authenticated. Tags help filter posts by topic. 

- Series
- Articles
- Comments
- Tags

## OPEN REQUIREMENTS

MVP:
Owner can create series and write articles under a series.

COMPLETED FEATURES:
- Add role-based access
- add image service
- Add email service for registration and contact me form
- Implement tags 
- Slug service (alternate routes for accessing articles instead of primary keys)
- Visitors may add comments after registering and logging in. 
- Locate comments by guest
- Add role-based views
- user can click tags to find other articles with that tag
- Implement Series as a nav bar in shared _layout with searcher
- Article cards for landing page
	- featured article with photo, series, title, and summary (links to article)
	- 2nd-5th most recent articles below featured article at half size
- Series index
	- featured article with photo series, title, and summary (links to article)
	- 2nd-5th most recent articles below featured article at half size
- Article page
	- Series
	- Title
	- Summary
	- AuthorImage Author
	- Article Image
	- Article Body
	- Article Modals for comments
- create modals for editing comments
- implement front-end styling in HTML and CSS. 
- reroute series pages to link to an index of articles within that series instead of a series detail page

FUTURE UPDATES:
- configure social previews
- add sharing links options
- create demo role and account that can leave anonymous comments and not modify them. 
- Extend slug service to Series
- create modals for editing series titles/descriptions/pictures
- Show/Hide comments
- Hover series to display carousel of articles within that series
- Add a method to reply to comments. 

## USER INTERFACE
Dashboard shows series and recent articles. Side-menu to older articles. Search function. Login for writing articles or comments. 

## LOGIC DESIGN
Identity Access, owner creates posts
Role Based Security, authenticated visitors may leave comments

## DATA DESIGN
- Blog Series
- Blog Article
- Blog Tag
- Blog Comment
- Photos

-- Users--
- Photo
- Contact Links
- Collection<Articles
- Collection<Comments

--Blog--
- Name
- Description
- Date Created
- Date Updated
- fk_Image
- fk_Creator
-Collection<Articles

--Comment--
- Subject
- Comment
- Date Created
- Date Updated
- Date Deleted
- fk_Article
- fk_creator

--File--
- IFormFile (Image)
- PhotoName
- PhotoExtension
- PhotoData
- DateUploaded

--Article--
- Title
- Summary
- Body
- Status
- Date Created
- Date Updated
- Slug
- Photo
- fk_series
- fk_creator
- Collection<Tags
- Collection<Comments

--Tag--
- Tag
- fk_post


