# Who Knew A Follow Button Could Be So Complex?
July 13, 2025

So I recently got to a point in the development of Crate, where I needed to add follow buttons to user profiles. Little did I know it would be much much more than just adding a simple little button to a page. And yes I know it's a meme, "front end dev spends yet another entire 8 hour work day making sure the button color is just right", but I just wanted it to look perfect for you guys. But really, given I haven't ever built out something where users would even need an option to follow other users, I didn't quite realize the many different things that would need to be implemented or data pulled/sent to make sure it behaves the way you would expect. 

Let me list them, at least the one's I've realized so far:

    - Check if user currently signed in
        - How:
            - Get session data
            - Check if user is viewing own profile
                - How:
                    - Determine profile being viewed
                    - If user signed in, get user id
                    - Get username by user id
                    - Compare profile to username
                    - Check if already following:
                        - How:
                            - Get signed in user's id
                            - Get user id of profile being viewed
                            - Check table for relationship

And while it's clearly not the longest list of things you've ever seen, it's definitely wasn't the first thing that crossed my mind when thinking "Oh yeah I need to add the follow button to this page". So next time give that front end dev some slack, they really might be working on that button till EOD.
