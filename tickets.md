# GitHub support tenets: a tl;dr

### Logic + empathy

It's a satisfying balance to bring both analytical skills to a problem, but also remember to respond to a user with care.

### Transparency + honesty

We put effort into writing up [post-mortem blog posts about What Went Wrong](https://github.blog/2022-03-23-an-update-on-recent-service-disruptions/). The balance here is to show enough transparency so users feel respected, but in the case where things are horribly wrong, not share so much that we overwhelm them.

[Here's an example of a support request](https://gist.github.com/3e89df1f7c0e7d6d5737). It may be easier to say something vague and not-technically-untrue like "there was a small problem and we fixed it". It means we don't have to cop to a mistake on our end. Our users are in the tech world, and are used to figuring out problems. We have found we're much better off telling them what's up, and why.

### Surprise + delight

We have an awesome user base, who generally think we're pretty great. We've put a lot of social effort into meetups, conference talks and blog posts that wow people and create fans of our company and the products we [ship](http://shipitsquirrel.github.io/images/ship%20it%20squirrel.png).

We follow the [Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service), and go above and beyond when it's appropriate. We have the ability to refund as much as we want, and to offer coupons as often as we want. We use this judiciously, as you can turn a surprise into disappointment if wielded badly. You can go back to logic+empathy to consider if what you'd like to do will actually delight the user.

Often, our users may just need information quickly and clearly, without being goofy. We have to know how to respond in the way that best matches how the user is feeling.

## GitHub voice

To explain it casually, we try to exude something that sounds like the person:

* is a real human
* is invested in things going well for you (we care)
* is really smart, but kind (not egotistical)
* and maybe kind of funny (good robot test)
* or at least interesting (and also not actually a robot)
* is not businessy
* could be found in a hoodie, blaring music, slouching in a bean bag chair

## Humble brag

Here's what someone wrote about us, in a longer piece about moving their company to GitHub:

> This leads me to the Customer Service itself. The GitHub staff I’ve been in contact with is extremely helpful, efficient, and comprehensive of our specific requirements. Most important: you deal with real people with real names, not with an anonymous service. When a member of the support staff takes your case (which happens in minutes, even for us Europeans), you get in touch with this person each time you interact on the case. And their CRM tools seem good enough so that your customer history is quickly available to all the support staff. I must say that I didn’t expect such a good customer service from a company with a reputation of automating everything they can, but they really take customer relationship seriously.

## An FYI on how we work

Most of the support team is remote, so we use a group chat room and a support app to work together. We also use GitHub -- it's where the code is stored, where we log bugs, and where we collaborate on new ideas. We don't tend to email or call each other, though we'll videochat every once in a while to catch up. Mostly we hang out in the support chat room to communicate.



# Support tickets

Please read the 3 tickets provided below, and reply by removing _replace this with your response_, replacing it with your response.

Please make sure you don't change anything else in this file. Just add your responses to the proper sections. Also, please make sure your editor is saving the file using the UTF-8 character encoding.

Having trouble getting an answer? That's okay! Walk us through your research technique, what you've tried, and where you're getting stuck so we can see your thought process instead.

Good luck!



## Ticket #1: Rejected pull request from fork

> To start, I have to say I LOVE GITHUB. You guys rock. I was at your 4th birthday party, thanks for the cupcake and booze!
>
> Anyway, here's my problem. I sent a pull request to technoweenie, and he rejected it because my master branch is out of sync with his master. What can I do to fix this?
>
> Help me supportocat, you're my only hope!
>
> /.Steve

Hint: You'll want to address their question, and you could add an explanation of topic branches as a better workflow.


### Ticket #1 response:

Hi Steve,
>
Hope you are doing well & thanks for your wishes, we are looking forward for you to attend our 5th Birthday party as well :) 
>
The pull request status may be rejected due to several factors, such as code complexity, code quality, the number of changed files, etc.

Initally you can try command as "git pull upstream master" your pull request is done from a dedicated branch, not from master.
If that doesnt help, you can try the below steps.

>git fetch upstream
>git checkout my_PR_branch
>git rebase upstream/master
>git push --force

>To know more about topic branches you can also refer to this 
https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows

Let us know how it goes and if that does help your master brach to sycnh with technoweenie master brach.
>
>Br,
>Dharmik 

(NOTE: I am also thinking to suggest the customer to create a new branch save the work, and synch the master branch with it.
 as i dont have whole insight on this i would prefer to consult some experts and then suggest the customer also wait for his next response at same time.) 

## Ticket #2: Syncing internal server and GitHub?

> Hi GitHub! My company has an internal Git server used for deployments, we use GitHub, and I work on a local copy of the repository. For workflow purposes, how do I sync my repository to GitHub and the internal Git server?
>
> Thanks,  
> vmg

Hint: One common option is Git remotes. There are others!


### Ticket #2 response:

Hi VMG, 
>
Hope you are doing well, and thanks for reaching us out. 
> 
In regards to your query, You can sync your internal git repository with GitHub adding a remote repository.
To add a GitHub remote to your internal repository, you can do:

$ git remote -v
>origin	https://your-internal-repo.com/group/project (fetch)
>origin	https://your-internal-repo.com/group/project (push)

>$ git remote add gh https://gitHub.com/group/project
>$ git remote -v
>origin	https://your-internal-repo.com/group/project (fetch)
>origin	https://your-internal-repo.com/group/project (push)
>gh	https://gitHub.com/group/project (fetch)
>gh	https://gitHub.com/group/project (push)
>
Let us know how it goes. 
>
Br,
>Dharmik 



## Ticket #3: Unhappy about forking

> JamesTK here, I have another question.
>
> One of my dev collaborator forked my private repo without explicit permission to do so... is that typical? I am surprised that the system did not notify me if it was okay to grant the fork permission. Is there a way to setup permissions of this sort? Also, other than asking the collaborator to delete the forked repo, can I actually delete it?
>
> Thanks, jamestk

Notes:

You've checked the account in our admin view, he only has one personal repository (jamestk/tribbles), which has one collaborator. Any documentation you may need is available on [help.github.com](https://help.github.com).


### Ticket #3 response:

Hello Jamestk,
>
>Thank you for reaching us out for this matter, we understand your disappointment that one of your Dev collaboratar fork it without your permission :(  
>
>i will clear it for you, in a private repository, repository owners can only grant write access to collaborators. 
Collaborators can’t have read-only access to repositories owned by a user account, which is why the Dev was able to fork it.
>
>More information about permission levels for a repository owned by a user account can be found here:
https://help.github.com/articles/permission-levels-for-a-user-account-repository/
>
>For Forking permission you can refer to this 
https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-the-forking-policy-for-your-repository
>
>Yes you can delete the repo by yourself below steps will help you
>
>1.Click to your repository for example yourUsername/yourRepository for example dharmik/test.
>2.Then in the main toolbar of GitHub click on Settings
>3.Scroll to the bottom of the page to the section called Danger Zone and you will find Delete this repository button
>4.When you click it another pop up will appear here you need to type in your Github username and the name of your repository in this format gitHubUsername/nameOfTheRepository and click on the button below which says: I understand the consequences, delete the repository
>
Br,
Dharmik


## Love to know more about yourself

We'd also love if you could share more about yourself so the team can get to know you better! If you could fill the following out that would be great:

### Name?

Dharmik Mehta

### Location?

Mumbai,India & Kuala Lumpur,Malaysia

### What's an impressionable experience you've had with customer service/support, and why?

Working for a company called Microsense India PVT LTD made me realize that service / support is one of the important 
function for any business and its plays a make or brake role between customers and Company hence this is why.

### Tell us about a time where you helped someone.

The list is long and i might have to write a book on this, last time it was where one of the enduser was not able to install the application on a server found out that from registry the option to auto update the TLS certs is turned off and most of the cloud based application needs the certs to be up to date hence i helped him to debug it and resolve it as well.

### What appeals to you about GitHub, as a company you'd potentially be working for?

I have come across GITHUB website's many time in my life and i've realize it, that it plays one of the important role for automation or software developement in 21st century this is why i want to be part of it.

### How would you describe what GitHub does to a non-technical person?

Just like a vehicle( car) goes through assembly line for developement just like that GITHUB is a production plant for software along with a garage at the same time 

### What motivates you to work in support?

Helping customers and being a bridge between R&D and customers at same time motivates me to work in support.

Thanks for taking the time and effort to tell us more about yourself. We look forward to reading your responses.

## Final step

Make sure you save this file. And that your editor is saving it using the UTF-8 character encoding. Go back to the email you received from us, and upload this file to the unique link you will find at the bottom of the email.

Thanks!


