# salesforce-developer-console-fix

## Summary
This VisualForce pages clears the current Salesforce user's developer console state.

You know how sometime the Salesforce Developer Console sometimes hangs up? It stops loading, but does not provide any error message. If you look at the javascript console, you see that it has encountered an error and silently crashed.

Googling for [salesforce developer console not loading](https://www.google.com/search?client=safari&rls=en&q=salesforce+developer+console+not+loading), I found that [Salesforce help gives a procedure](https://help.salesforce.com/articleView?id=000205964&language=en_US&type=1) for fixing this, but it's kind of a pain, involving sleuthing through the Developer Console's network interactions to find the Id of the state (the IDEWorkspace), and using the [Workbench](https://workbench.developerforce.com/login.php) to delete it.

This VisualForce page gives you a button that does that for you. 

### Installation

Because it's a VisualForce page, with no server side code and no static resources, it's dead-simple to install into your Salesforce instance (even production). Just create a VF page, and copy and paste this code from [DeveloperConsoleFix.page](https://github.com/bolaurent/salesforce-developer-console-fix/blob/master/DeveloperConsoleFix.page) (view it as raw). If your page is named DeveloperConsoleFix, the url will be /apex/DeveloperConsoleFix.

### Kudos

Thanks to [stomita](https://github.com/stomita) for the amazing https://jsforce.github.io library, which provides access to all the Salesforce APIs.

