# ModernBusiness.OrchardCore
Theme for Orchard Core based on the Modern Business theme of Start Bootstrap

See the [README](https://github.com/psijkof/ModernBusiness.OrchardCore/blob/master/wwwroot/README.md) file of the embedded theme repo.

The goal is to implement this template as efficiently as possible with [Orchard Core](https://github.com/OrchardCMS/OrchardCore) 


# Status and implementation details

## Modern Business Theme, content type
 
* Content model 
* Services 
* Service 
* Portfolio 
* Project 
* Pricing 
* PrincingPlan 
* FAQ 
* QuestionAnswer 
* Team 
* Customers 
* Blog 
* BlogPost 
 
 
## Pages  
* Homepage 
* About 
* Services 
* Contact (Workflow form validation and submit) 
* Portfolio pages 
  * 3 Column Portfolio 
  * Single Portfolio item (via link on portfolio summary) 
* Blog Home 2 
* Blog Post (search and categories still hard coded) 
* Faq 
* Pricing Table 
 
## Details 
* Breadcrumb 
* Zones and Layers 
* Widgets 
  * Carousel 
  *Footer 
* Pageheader (containing breadcrumb) 
* Menu (see issues) 
* Blog Comment section – Used Disqus 
 
## Approach 
Using Page content type with Flow part, provides some extra control over how to display content without much effort, mainly useful if Page contains several sections each with different types of content (Homepage) 
 
## Queries 
Used Lucene queries to retrieve content by its type, example: 
```
{
  "query": {
    "term" : { "Content.ContentItem.ContentType" : "Project" } 
  }
} 
```

## Issues 
 
* Pagination – No idea/documentation on how to create pagination from queried items 
  * Also, no information on how to create templates for pagination 
* Search 
  * Search box on the Blog summary page is not implemented.  
* Homeroute / menu routes has an issue 
  * Reported issue #2399 
 
