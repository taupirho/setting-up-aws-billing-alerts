# setting-up-aws-billing-alerts

In one of my [LinkedIn Posts](https://www.linkedin.com/posts/tom-reid-5a2a3a_if-you-are-a-user-of-aws-keep-in-mind-that-activity-6564431727945625600-irbo) I highlighted how you can be caught out by a large and unexpected bill from AWS if you’re not careful. 
This can happen even when you’re on the free tier since,
```
a) not all services are free and 

b)some services can rack up the costs even when you’re not using them!
```
It was a salutary lesson and my parting advice on that post was that you should set up billing alerts so that you don’t receive any nasty shocks. It occurred to me that many of you – especially new AWS users - might not know how to set up billing alerts. If that’s you, this article will show you how.

Login to your AWS account.

Near the top left of the screen you’ll see a Services drop-down list. Click on it then enter the term “budget” into the search box that appears.

Choose AWS Budgets, then click on the **Create Budget**  button near the top right-hand side of the screen.

On the next screen, you want to make sure the Cost Budget option is selected, then click on the **Set Budget** button near the bottom right hand side of the screen.

On the next screen you’ll need to fill out your budget name, the period of the monitoring e.g. Monthly, Quarterly or Annually and your budgeted amount. For the period chosen you can decide whether you want the period selected to repeat or last for a fixed interval. The amount you enter for your budgeted amount is up to you, but I would suggest $5 to $10 for a Monthly budget is a good option if you’re on the free tier, say, and a light user. If you find that you’re always exceeding your budget you can revise it upwards. However, make sure 
you know exactly why this is happening. It could be because there are services which are racking up costs that you’re not aware of.

Once you’ve chosen all the required options you can move on to the next screen by clicking on the **Configure Alerts** button near the bottom right hand corner of the screen.

You can configure up to five alerts which will be more than enough for most users but if you need more than five you can always set up more budgets and get another five alerts for each of those too. 

First, choose on what basis you want the alert to fire – for actual costs or forecasted cost. Forecast cost is where AWS works out a predicted monthly, quarterly or annual cost for you based on your actual daily usage costs.  Actual cost is your actual spend of course.

Next, choose what percentage of your budget is to be reached before AWS alerts you.

Now, choose your method of contact by AWS. This can be either a straightforward message sent to an email address of your choice or a text message if you already have an AWS SNS topic set up to go.

When you’re done, click on the Confirm Budget button near the bottom left hand side of the screen. You’ll be presented with a summary screen showing the alert details you’ve just set up. If you’re happy with these the final step is to click on the Create button at the bottom left of the screen and you’re alert will then be live.

I think a reasonable set up is to have four “actual cost” alerts that notify you when you’ve spent, say, 60%, 70%, 80% and 90% of 
your budget amount and one “forecast cost” alert that will notify you if your predicted cost over your chosen period is likely exceed
90% of your budgeted amount. Choose your own threshold values to suit your own circumstances and “fear factor”. Setting up your alerts
this way means you’re unlikely miss one even if you don’t check your email or mobile device for a while. 

My final piece of advice is **always, always** investigate the underlying cause if you do receive a billing alert.







