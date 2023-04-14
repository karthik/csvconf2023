# How to enable and sustain thriving Open Source Ecosystems (OSE)

[![][imgur]](https://inundata.org/talks/csvconf/#/0/3)

*[Slides][inundata] from a keynote presentation at [CSV Conf 2023][csvconf] in Buenos Aires, Argentina. April 19th, 2023*
## Abstract

Software impacts virtually all areas of research but has been a heavily undervalued contribution. Over the past decade alone, the research software landscape has changed dramatically. It is now substantially easier to start new software projects, find technical resources, and join a friendly community of practice. The research software engineer career track has also taken off and made it easier for many individuals to build careers in this field. However, several key challenges remain. Despite the growing recognition of research software, it is still challenging to demonstrate impact or find support for the maintenance of existing software. In this talk, I describe some ideas on how to uncover software that is driving research and construct knowledge graphs to ask questions about software use and sustainability. I also describe the various conditions necessary to turn nascent software projects into sustainable ecosystems.

## General takeaways 

- Since research software is poorly cited, it’s hard to get a good picture of the software used in research. While software bills of materials are technically easy to generate and will provide a lot of value, they are not the norm in research or publishing.
- One workaround is to extract scientific software entities from PDFs using tools like Grobid and the software mentions extractor. If carried out on a substantial collection of articles from a field where open source is widely used, it would be possible to ask all kinds of interesting questions like which software is driving research in a certain area, where the opportunities and challenges are, and how to use of tools is changing over time.
- Many researchers write last mile ‘analysis code’ that never goes any further. Some of this code, especially the implementation of new methods, may see the light of day as ‘prototype software’. These are minimum viable prototypes, with a small test suite and documentation but not designed for speed or stability. A subset of prototypes that find product-market fit are the ones that enter the research software infrastructure space and need to be sustained. 
- One way for software projects to raise their visibility is to align roadmaps with adjacent tools (adjacent in the sense of hard dependencies or usage-based dependencies). This would reduce friction, allow for resource sharing, and raise visibility as a collection of tools (eg. [spatial data science](https://r-spatial.org/), [Tidyverse](https://joss.theoj.org/papers/10.21105/joss.01686))
- Besides solving technical challenges by aligning with the local ecosystem, projects also need to be in alignment with the larger ecosystem (actors and institutions that enable the work).
- The definitions of software sustainability are clear, but a broader definition I provide is that “Software is sustainable as long as the people behind it have the resources to continue fulfilling its mission”.
- There are examples of widely used software that have run out of resources while dealing with an outdated stack. Rather than sustain those tools, the community can choose to replace them with something more modern and aligned with the needs of users (see the IRAF → Astropy example below). In other words, not everything needs to be sustained forever.
- At [POSE training](https://pose.training/), we have identified 5 core areas that are necessary to sustain an OSE. These are org structure (the managing org that can guide future growth), governance (robust decision-making and collaboration management), business perspectives (a good way to manage hidden infrastructure costs and resources, which includes funding), security (technical and non-technical threats), and community. 
- Using Nadia Eghbal’s taxonomy (toy, club, federation & stadium), it would be a good exercise to categorize your project to see how best to engage your audience in meaningful ways. 
- Once projects have found product-market fit, there is little in the way of long-term support (funding or otherwise). COPs (and Ecosystem-level entities) can use tools like [CHAOSS](https://chaoss.community/) to surface certain types of issues (low maintainer growth, time to PR close as a way to engage new contributors) and address those before it is too late to address them. 
- Security issues are important. While we have not seen major security issues in scientific open source (compared to the larger OSS community), it is still important to stay on top of CVEs and use CI/CD more extensively. It would also be a good idea to keep an eye on non-technical threats, like bad actors, and poor governance.
- If all else fails and a project needs to end, it must be done responsibly. This includes notifying all stakeholders (downstream dependencies, users, trainers), pointers to comparable alternatives, archiving all code to support reproducibility efforts, and providing enough lead time (See the r-spatial example below).
- The calls to action are:
	- If you are a developer, find ways to align with your local ecosystem to coordinate roadmaps and resources, and raise your visibility
	- If you’re a COP, find ways to support maintainer burnout, support governance templates, document managing org options etc.
	- Lastly, folks operating at the level of an ecosystem (funders, foundations, training partners, infrastructure providers) can also pick and address one or more of these issues at scale. 

## Resources

- [The Journal of Open Source Software][theoj]   
	* Paper about the design of The Journal of Open Source Software (JOSS): [Journal of Open Source Software (JOSS): design and first-year review][peerj]
- [Software Bill of Materials][synopsys]
- [Transitive Credit as a Means to Address Social and Technological Concerns Stemming from Citation and Attribution of Digital Products][metajnl] Dan Katz and Arfon Smith
- Grobid, [][readthedocs]![](https://i.imgur.com/hIzjbUo.png)   
- [Softcite dataset: A dataset of software mentions in biomedical and economic research publications][onlinelibrary] Caifan Du, Johanna Cohoon, Patrice Lopez, James Howison   
- [Mining Software Entities in Scientific Literature: Document-level NER for an Extremely Imbalance and Large-scale Task][acm] Patrice Lopez, Caifan Du, Johanna Cohoon, Karthik Ram, James Howison  
- [Pathways Enabling Open Source Ecosystems training program][pose] part of the NSF’s TIP directorate [POSE program][nsf]      
- [Software Sustainability: Research and Practice from a
Software Architecture Viewpoint][hud] (PDF)
- [Report: Sustainability in Research-Driven Open Source Software][codeforsociety] - Danielle Robinson and Joe Hand      
- Perry Greenfield’s PyData Keynote on [How Python Found its way Into Astronomy][youtube] covers some of the transition from IRAF → AstroPy      
- [Working in Public: The Making and Maintenance of Open Source Software][stripe] 📙      
	- [Roads and Bridges: The Unseen Labor Behind Our Digital Infrastructure][fordfoundation] *This is an older report and has some of the ideas from the book in case you can’t get a hold of that one* 
- [CHAOSS Community][chaoss] *stands for Community Health Analysis for Open-Source Software.*
- Various links from [The rOpenSci Project][ropensci]  
	- [Thanking Your Reviewers: Gratitude through Semantic Metadata][ropensci]    
	- [rOpenSci Dev Guide][ropensci]
	- [rOpenSci Champions Program][ropensci]  
	- [rOpenSci Review Tools][github]   
- [r-universe][r-universe]
	- [CRAN to Git][ropensci]: How to use r-universe to search across package ecosystems.
- [CSCCE community participation model][cscce] *They also run a [Community Engagement Fundamentals course][cscce] designed for STEM community managers*
- [Strategy for Culture Change][cos] *[Nicholas Tierney][njtierney] and I adapted this concept in a paper about [data sharing][sciencedirect]*. Here’s a [direct link][els-cdn] to our figure.
- On the topic of software being retired, here is a series of posts ([part 1][org/r/2022/04/12/evolution], [part 2][org/r/2022/12/14/evolution2], [part 3][org/r/2023/04/10/evolution3]) about rgdal and other tools in the R spatial suite being retired in fall 2023 because the core maintainer is retiring and the stack has been replaced by something better. Note all the steps being taken to retire this responsibly 
> “ We describe where their functionality will go, what package maintainers can or should do, and which steps we will take to minimize the impact on dependent packages and on reproducibility in general.”

## How to cite this talk

```Ram, Karthik. (2023, April 12). How to enable and sustain thriving Open Source Ecosystems (OSE). Zenodo. https://doi.org/10.5281/zenodo.7822917```

## Acknowledgements

This talk was greatly improved by discussions with [Arfon Smith](https://www.arfon.org/), [James Howison](http://james.howison.name/), [Sean Goggins](https://www.seangoggins.net/), [Patrice Lopez][science-miner], and [Abby Cabunoc Mayes](https://abbycabs.github.io/). 

## Questions

Questions or comments are welcome at karthik dot ram at gmail.



[science-miner]: https://science-miner.com/
[org/r/2023/04/10/evolution3]: https://r-spatial.org/r/2023/04/10/evolution3.html
[org/r/2022/12/14/evolution2]: https://r-spatial.org/r/2022/12/14/evolution2.html
[org/r/2022/04/12/evolution]: https://r-spatial.org/r/2022/04/12/evolution.html
[els-cdn]: https://ars.els-cdn.com/content/image/1-s2.0-S2666389921002300-gr1_lrg.jpg
[sciencedirect]: https://www.sciencedirect.com/science/article/pii/S2666389921002300
[njtierney]: https://www.njtierney.com/about/
[cos]: https://www.cos.io/blog/strategy-for-culture-change
[cscce]: https://www.cscce.org/trainings/cef/
[cscce]: https://www.cscce.org/resources/cpm/
[ropensci]: https://ropensci.org/blog/2023/04/03/cran-to-git/
[r-universe]: https://r-universe.dev/search/
[github]: https://github.com/ropensci-review-tools
[ropensci]: https://ropensci.org/champions/
[ropensci]: https://devguide.ropensci.org/
[ropensci]: https://ropensci.org/blog/2018/03/16/thanking-reviewers-in-metadata/
[ropensci]: https://ropensci.org/
[chaoss]: https://chaoss.community/
[fordfoundation]: https://www.fordfoundation.org/work/learning/research-reports/roads-and-bridges-the-unseen-labor-behind-our-digital-infrastructure/
[stripe]: https://press.stripe.com/working-in-public
[youtube]: https://www.youtube.com/watch?v=uz53IV1V_Xo&t=11s
[codeforsociety]: https://www.codeforsociety.org/resources/report-sustainability-in-research-driven-open-source-software
[hud]: https://eprints.hud.ac.uk/id/eprint/33972/1/1-s2.0-S0164121217303072-main.pdf
[nsf]: https://beta.nsf.gov/funding/opportunities/pathways-enable-open-source-ecosystems-pose
[pose]: https://pose.training/
[acm]: https://dl.acm.org/doi/abs/10.1145/3459637.3481936
[onlinelibrary]: https://asistdl.onlinelibrary.wiley.com/doi/abs/10.1002/asi.24454
[readthedocs]: https://grobid.readthedocs.io/en/latest/Principles/
[metajnl]: https://openresearchsoftware.metajnl.com/articles/10.5334/jors.be
[synopsys]: https://www.synopsys.com/blogs/software-security/software-bill-of-materials-bom/
[peerj]: https://peerj.com/articles/cs-147/
[theoj]: https://joss.theoj.org/
[pose]: https://pose.training/
[theoj]: https://joss.theoj.org/papers/10.21105/joss.01686
[r-spatial]: https://r-spatial.org/book/
[csvconf]: https://csvconf.com/
[inundata]: https://inundata.org/talks/csvconf/#/0/3
[imgur]: https://i.imgur.com/VjeqIqr.jpg
