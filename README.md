<img align="middle" src="http://c.mfcreative.com/mars/landing/lohp/2014/smp/us-lohp-simplehdr-logo.png" alt="Ancestry.com"/>
<img align="right" src="http://thinkbig.teradata.com/wp-content/themes/thinkbig/images/header/Logo128.png" alt="Think Big"/>


# Think Big Challenge 2014

> 
> Already finished? Then jump to [the submission page!](https://thinkbigchallenge.wufoo.com/forms/think-big-and-ancestrycom-challenge-2014)
> 

Think Big and Ancestry.com have partnered to present this Big Data challenge for Strata NY 2014. Whether you're a Data Scientist, Engineer, or Architect -- this is your chance to show off your Big Data skills with a very interesting data set from Ancestry.com. In addition to competing for prizes (like a $200 Apple Store gift card), winning entries will be featured on our web site and may be included in our webinar series.

## Introduction

This contest is based on a rich genealogy data set from Ancestry.com where each member can create and maintain an individual family tree. Since members may share common ancestors, there will inevitably be some overlap between trees. Identifying, matching, and de-duplicating these overlaps, at scale, is a significant challenge.

### About the data

The contest data set consists of over JSON-encoded family tree records in a flat file. Some preprocessing has been performed on the data, such as standardizing place names and obscuring family names to protect member privacy, and is described in the documentation.

Documentation of the record format, a small extract, and links to downloads may be found in the `data` directory in the [github repo](https://github.com/ThinkBigAnalytics/ThinkBigChallenge2014/tree/master/data).

## The Challenge

Implementing (or even designing) a complete solution to match and de-duplicate these trees is well beyond the scope of any single contest lasting for just a few days (or weeks!). However, as with any "big" problem, you can make progress on a number of interesting pieces along the way. The judges are interested in your approach--including which aspects you choose to tackle.

We have no expectations or requirements to use specific platforms, programs, languages, packages, etc. **Impress us.**

Multiple prizes will be awarded, and we welcome multiple submissions for any or all of the following challenges:

### Data Engineering Challenges

**Detect Exact Matches.** The data set contains some true duplicates, where every data element matches except for the id. Try detecting these duplicates as first step. The judges will be interested in your selection of tools and your presentation of your rationale.

**Create Trees from Provided Matches.** Construct family trees starting with the earliest ancestors identifiable by the matching gids already present in the data. 


### Data Science Challenges

**(Un/Semi)Supervised Learning of Common Ancestors.**  You have two datasets: a large file (AncestryPost1820Data.gz) containing records for persons born after 1820; a small sample file of persons born before 1820.  Use this to build a system that identifies family tree branches whose earliest ancestors in AncestryPost1820Data have common parents (pre-1820). This should be done for the immediate parent of the branch root in AncestryPost1820Data.

Winners are selected for having the most accurate solution.

**Visualizing Naming Norms.**  Identify trends and patterns in how children are named across regions, families, or other strata; create a visualization to share this insight.  Data sampling is encouraged for contestants who cannot work with the full dataset.

Winners are selected for novelty of insight, creativity, and quality of visualization.


## How to Enter

The contest submission form is here: [https://thinkbigchallenge.wufoo.com/forms/think-big-and-ancestrycom-challenge-2014](https://thinkbigchallenge.wufoo.com/forms/think-big-and-ancestrycom-challenge-2014).

The contest officially ends at Sunday (10/19) at 11:59pm EDT.  However, the form will continue to run through the following Friday.  We will do our best to review any late submissions.  The most important thing is have fun and do something amazing!


* * *

## Contest Official Rules

**NO PURCHASE NECESSARY**

**HOW TO ENTER:** This contest starts on 10/16/2014 at 10:30am EDT and
ends on 10/19/2014 at midnight EDT.

**1. PARTICIPATION.** Participation in this contest constitutes your
full and unconditional agreement to and acceptance of these Official
Rules and the decisions of Sponsor, which are final in all respects. To
enter, you must complete the challenge. No mechanically reproduced
entries accepted. Sponsor and its agents are not responsible for
incomplete, lost, late, damaged, illegible or misdirected entries, which
will be deemed ineligible. Entries become Sponsor's property and will
not be returned.

**2. ELIGIBILITY:** This contest is open only to any legal working
residents of the United States, 18 years of age or older at time of
entry. Void in Puerto Rico and the Province of Quebec, and where
prohibited by law. Employees (including immediate family members and/or
those living in the same household of each) of Sponsor, its advertising,
promotion and production agencies, the affiliated companies of each, and
the immediate family members of each are not eligible.

**3. AWARDING of PRIZES:** On or about October 20, from among all
eligible entries Ð a panel of sponsor judges will determine the winners
based on completeness of entry.

**4. PRIZES:** Based on the judge's decision, the following prize(s)
will be awarded:

* One Apple Store gift card (Approximate Retail Value: $200.00) 
* 2nd & 3rd place prizes of lesser value will also be awarded

ALL TAXES ON THE PRIZES ARE THE SOLE RESPONSIBILITY OF THE WINNERS OR
WINNERS' DESIGNATED RECIPIENT. Sponsor will notify winners by telephone,
mail or e-mail, at Sponsor's discretion. No substitutions or cash
awards, except that Sponsor reserves the right to substitute a prize of
equal or greater value in the event of unavailability.

**5. CONDITIONS OF PARTICIPATION:** In the event of noncompliance with
these requirements, the selected entrant may be disqualified and an
alternate winner selected, at Sponsor's discretion. Sponsor reserves the
right to suspend, cancel or modify this promotion if fraud or any other
causes beyond its control destroys the integrity of the promotion, as
determined by Sponsor's sole discretion. If the promotion is cancelled,
unawarded prizes may be returned to Sponsor or may be awarded by random
drawing from eligible entries, to the extent a fair random drawing can
be conducted, at Sponsor's discretion.

**6. GENERAL:** All federal, state and local laws and regulations apply.
By accepting prize, winners consent to Sponsor's use of their names and
likenesses without additional compensation, unless prohibited by law. By
entering the contest, you release and hold harmless Sponsor, its parent,
subsidiaries, affiliates, employees and agents from any and all
liability or any injuries, loss or damage arising from or in connection
with participation in this promotion or acceptance/use of the prize.

**7. SPONSOR:** The sponsor of this promotion is Teradata Corporation,
10000 Innovation Drive, Miamisburg, Ohio 45342.

