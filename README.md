# How to enable and sustain thriving Open Source Ecosystems (OSE)

[![](https://i.imgur.com/VjeqIqr.jpg)](https://inundata.org/talks/csvconf/#/0/3)

*[Slides](https://inundata.org/talks/csvconf/#/0/3) from a keynote presentation at [CSV Conf 2023](https://csvconf.com/) in Buenos Aires, Argentina. April 19th, 2023*
## Abstract

Software impacts virtually all areas of research but has been a heavily undervalued contribution. Over the past decade alone, the research software landscape has changed dramatically. It is now substantially easier to start new software projects and find a friendly community of practice, and technical resources. The research software engineer career track has also taken off and made life easier for many individuals. However, several key challenges remain. Despite the growing recognition of research software, it is still challenging to demonstrate impact or find support for the maintenance of existing software. In this talk, I describe some ideas on how to uncover software that is driving research and construct knowledge graphs to ask questions about software use and sustainability. I also describe the various conditions necessary to turn nascent software projects into sustainable ecosystems.

## General takeaways 

- Since research software is poorly cited, so it’s hard to get a good picture of the software used in research. While software bills of materials are technically easy to generate and will provide a lot of value, they are not the norm in research or publishing.
- One workaround is to extract scientific software entities from PDFs using tools like Grobid and the software mentions extractor. If carried out on a substantial collection of articles from a field where open source is widely used, it would be possible to ask all kinds of interesting questions like which software is driving research in a certain area, where the opportunities and challenges are, and how to use of tools is changing over time.
- Many researchers write last mile ‘analysis code’ that never goes any further. Some of this code, especially the implementation of new methods, may see the light of day as ‘prototype software’. These are minimum viable prototypes, with a small test suite and documentation but not designed for speed or stability. A subset of prototypes that find product-market fit are the ones that enter the research software infrastructure space and need to be sustained. 
- One way for software projects to raise their visibility is to align roadmaps with adjacent tools (adjacent in the sense of hard dependencies or usage-based dependencies). This would reduce friction, allow for resource sharing, and raise visibility as a collection of tools (eg. [spatial data science](https://r-spatial.org/book/), [Tidyverse](https://joss.theoj.org/papers/10.21105/joss.01686))
- Besides solving technical challenges by aligning with the local ecosystem, projects also need to be in alignment with the larger ecosystem (actors and institutions that enable the work).
- The definitions of software sustainability are clear, but a broader definition I provide is that “Software is sustainable as long as the people behind it have the resources to continue fulfilling its mission”.
- There are examples of widely used software that has run out of resources while dealing with an outdated stack. Rather than sustain those tools, the community can choose to replace them with something more modern and aligned with the needs of users (see the IRAF → Astropy example below). In other words, not everything needs to be sustained forever.
- At POSE training, we have identified 5 core areas that are necessary to sustain an OSE. These are org structure (the managing org that can guide future growth), governance (robust decision-making and collaboration management), business perspectives (a good way to manage hidden infrastructure costs and resources, which includes funding), security (technical and non-technical threats), and community. 
- Using Nadia Eghbal’s taxonomy (toy, club, federation & stadium), it would be a good exercise to categorize your project to see how best to engage your audience in meaningful ways. 
- Once projects have found product-market fit, there is little in the way of long-term support (funding or otherwise). COPs can use tools like CHAOSS to surface certain types of issues (low maintainer growth, time to PR close as a way to engage new contributors) and address those before it is too late to address them. 
- Security issues are important. While we have not seen major security issues in scientific open source (compared to the larger OSS community), it is still important to stay on top of CVEs and use CI/CD more extensively. It would also be a good idea to keep an eye on non-technical threats, like bad actors, and poor governance.
- If all else fails and a project needs to end, it must be done responsibly. This includes notifying all stakeholders (downstream dependencies, users, trainers), pointers to comparable alternatives, archiving all code to support reproducibility efforts, and providing enough lead time. 
- The calls to action are:
	- If you are a developer, find ways to align with your local ecosystem to coordinate roadmaps and resources, and raise your visibility
	- If you’re a COP, find ways to support maintainer burnout, support governance templates, document managing org options etc.
	- Lastly, folks operating at the level of an ecosystem (funders, trainers, infrastructure providers) can also pick and address several of these issues at scale. 

## Resources

- [The Journal of Open Source Software](https://joss.theoj.org/)   
	* Paper about the design of The Journal of Open Source Software (JOSS): [Journal of Open Source Software (JOSS): design and first-year review](https://peerj.com/articles/cs-147/)
- [Software Bill of Materials](https://www.synopsys.com/blogs/software-security/software-bill-of-materials-bom/)
- [Transitive Credit as a Means to Address Social and Technological Concerns Stemming from Citation and Attribution of Digital Products](https://openresearchsoftware.metajnl.com/articles/10.5334/jors.be) Dan Katz and Arfon Smith
- Grobid, https://grobid.readthedocs.io/en/latest/Principles/
![](https://i.imgur.com/hIzjbUo.png)   
- [Softcite dataset: A dataset of software mentions in biomedical and economic research publications](https://asistdl.onlinelibrary.wiley.com/doi/abs/10.1002/asi.24454) Caifan Du, Johanna Cohoon, Patrice Lopez, James Howison   
- [Mining Software Entities in Scientific Literature: Document-level NER for an Extremely Imbalance and Large-scale Task](https://dl.acm.org/doi/abs/10.1145/3459637.3481936) Patrice Lopez, Caifan Du, Johanna Cohoon, Karthik Ram, James Howison  
- [Pathways Enabling Open Source Ecosystems training program](https://pose.training/) part of the NSF’s TIP directorate [POSE program](https://beta.nsf.gov/funding/opportunities/pathways-enable-open-source-ecosystems-pose)      
- [Software Sustainability: Research and Practice from a
Software Architecture Viewpoint](https://eprints.hud.ac.uk/id/eprint/33972/1/1-s2.0-S0164121217303072-main.pdf) (PDF)
- [Report: Sustainability in Research-Driven Open Source Software](https://www.codeforsociety.org/resources/report-sustainability-in-research-driven-open-source-software) - Danielle Robinson and Joe Hand      
- Perry Greenfield’s PyData Keynote on [How Python Found its way Into Astronomy](https://www.youtube.com/watch?v=uz53IV1V_Xo&t=11s) covers some of the transition from IRAF → AstroPy      
- [Working in Public: The Making and Maintenance of Open Source Software](https://press.stripe.com/working-in-public) 📙      
	- [Roads and Bridges: The Unseen Labor Behind Our Digital Infrastructure](https://www.fordfoundation.org/work/learning/research-reports/roads-and-bridges-the-unseen-labor-behind-our-digital-infrastructure/) *This is an older report and has some of the ideas from the book in case you can’t get a hold of that one* 
- [CHAOSS Community](https://chaoss.community/) *stands for Community Health Analysis for Open-Source Software.*
- Various links from [The rOpenSci Project](https://ropensci.org/)  
	- [Thanking Your Reviewers: Gratitude through Semantic Metadata](https://ropensci.org/blog/2018/03/16/thanking-reviewers-in-metadata/)    
	- [rOpenSci Dev Guide](https://devguide.ropensci.org/)
	- [rOpenSci Champions Program](https://ropensci.org/champions/)  
	- [rOpenSci Review Tools](https://github.com/ropensci-review-tools)   
- [r-universe](https://r-universe.dev/search/)
	- [CRAN to Git](https://ropensci.org/blog/2023/04/03/cran-to-git/): How to use r-universe to search across package ecosystems.
- [CSCCE community participation model](https://www.cscce.org/resources/cpm/) *They also run a [Community Engagement Fundamentals course](https://www.cscce.org/trainings/cef/) designed for STEM community managers*
- [Strategy for Culture Change](https://www.cos.io/blog/strategy-for-culture-change) *[Nicholas Tierney](https://www.njtierney.com/about/) and I adapted this concept in a paper about [data sharing](https://www.sciencedirect.com/science/article/pii/S2666389921002300)*. Here’s a [direct link](https://ars.els-cdn.com/content/image/1-s2.0-S2666389921002300-gr1_lrg.jpg) to our figure.
- On the topic of software being retired, here is a series of posts ([part 1](https://r-spatial.org/r/2022/04/12/evolution.html), [part 2](https://r-spatial.org/r/2022/12/14/evolution2.html), [part 3](https://r-spatial.org/r/2023/04/10/evolution3.html)) about rgdal and other tools in the R spatial suite being retired in fall 2023 because the core maintainer is retiring and the stack has been replaced by something better. Note all the steps being taken to retire this responsibly 
> “ We describe where their functionality will go, what package maintainers can or should do, and which steps we will take to minimize the impact on dependent packages and on reproducibility in general.”

## How to cite this talk

```Ram, Karthik. (2023, April 12). How to enable and sustain thriving Open Source Ecosystems (OSE). Zenodo. https://doi.org/10.5281/zenodo.7822917```

## Acknowledgements

This talk was greatly improved by discussions with Arfon Smith, James Howison, Sean Goggins, Patrice Lopez, and Abby Cabunoc Mayes. 

## Questions

Questions or comments are welcome at karthik dot ram at gmail.

