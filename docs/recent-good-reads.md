# Recent Good Reads

A place where I share interesting coding-related stuff I find on the internet.

## Managing Python Versions

2022-05-24

I found this blogpost by **Logan Jones** on *realpython.com* why (and how) you should manage your python versions with pyenv. Perfect resource with all the important information on pyenv in one place.

Blogpost: [Managing Multiple Python Versions With pyenv](https://realpython.com/intro-to-pyenv/)

Additional Info:

I had some trouble installing pyenv on fedora 36. My solution:
1. Install the dependencies (as in the blogpost)
2. Install pyenv (as in the blogpost)
3. Install some python version (fails)
4. Install python version with verbose (-v) flag like `pyenv install -v 3.10.0`
5. check the output, google the commands on which the installation failed (for me it was missing `patch`)
6. install command with package-manager (for me `dnf install patch`)
7. back to 3. until you succeed

## Managing Dotfiles (Like A Superhero)  
2022-05-22

I've seen git repos of configuration files before, but never knew, how to do go about putting my computers config files into version management. Today I found the Answer. **Jake Wiesler** wrote a great blog article about it. I highly recommend the linked YouTube video aswell.

Blogpost: [Manage Your Dotfiles Like A Superhero](https://www.jakewiesler.com/blog/managing-dotfiles)  
Video: [Manage Your Dotfiles Like A Superhero](https://www.youtube.com/watch?v=FHuwzbpTTo0)

An interesting alternative approach was shared by **Nicola Paolucci** utilizing a bare git repository.

Blogpost: [The best way to store your dotfiles: A bare Git repository](https://www.atlassian.com/git/tutorials/dotfiles)

------

## (Maybe) Coming Soon to a Browser Near You: Temporal API 
Today I stumbled over a good read on handling date and time in code by one of the authors of the [Temporal API proposal](https://tc39.es/proposal-temporal/) on [Planet GNOME](https://planet.gnome.org). It once again shows how much more complex date and time handling are than you usually assume. That lead me to check out the Temporal API proposal, which is now something I'm really excited for.

In his blogpost Philip Chimento gives his thoughts on a tweet that caused quite some controversy:
> A couple of tough questions for all of you:
> 1. Is the date `2022-06-01` equal to the time `2022-06-01 12:00:00`?
> 2. Is the date `2022-06-01` between the time `2022-06-01 12:00:00` and the time `2022-12-31 12:00:00`?
> 3. Is the time `2022-06-01 12:00:00` after the date `2022-06-01`?

Enjoy!

Blogpost: [Comparing Apples and AppleOranges](https://ptomato.wordpress.com/2022/03/03/comparing-apples-and-appleoranges/)  
Additional Blogpost: [Is It Time for the JavaScript Temporal API?](https://blog.openreplay.com/is-it-time-for-the-javascript-temporal-api)

-------