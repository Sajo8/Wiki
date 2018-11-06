# TwitchTurtle Wiki

This is the repo for the [TwitchTurtle Wiki](https://docs.twitchturtle.com)

## Contributing Guidelines

You must follow [strict markdown](https://daringfireball.net/projects/markdown/), not GFM. Important points include-

* links must start with `../`, even if they're in the same directory, *if* the files are not in `docs/` (won't apply for `docs/filename.md` but will for `docs/folder/filename.md`)  
  ex -> `(../Rainborg-Wat-Dat)` instead of `(Rainborg-Wat-Dat.md)`

* relative links without the `.md` extension  
  ex-> `(Rainborg-Wat-Dat)` instead of `(Rainborg-Wat-Dat.md)`

* Links are *case sensitive*  
  Links to files in `mkdocs.yml` must *perfectly match* the casing of the actual files, and the links to these files from other places must *perfectly match* the casing in `mkdocs.yml`.


If:  

* (a) points are to be indented under one another,  

* (b) pictures/information are to be included under a "step 1",  

* (c) codeblocks are to be made under steps/points,   
     
     *they are to be indented by 4 spaces.*

* (d) *codeblocks must also start/end on a separate line.*

  **Note: Text given beyond this point wrapped in code blocks are just examples, observe the formatting and not what's written**

  #### Ex (a):

  ##### *Wiki MD*

   ```
   * Download wallet
     * Make a new wallet
       * give it a name
       ![walletname](wallets/images/name.png)
   ```

  ##### *Strict MD*

   ```
   * Download a wallet
       * Make a new wallet
           * give it a name
           ![walletname](images/name.png)
   ```

  #### Ex (b):

  ##### *Wiki MD*

   ```
   1. Download a wallet
   ![make wallet](wallets/images/make-wallet.png)
   ---
   In case you can't make, then just try again.
   ---
   2. Make a wallet
   Make sure you choose a strong password!
   3. Check that
     * it is saved [comfily](Being-Comfy).
   ```

  ##### *Strict MD*

   ```
   1.  Download a wallet
       ![make wallet](images/make-wallet.png)
       ---
       Incase you can't make, then just try again.
       ---
   2.  Make a wallet
       Make sure you choose a strong password!
   3.  Check that
       * it is saved [comfily](../Being-Comfy). (it assumed we are in the wallets/ directory)
   ```

   #### Ex (c) and (d):

   ##### *Wiki MD*
   ```
   1. Install Linux
   2. Enter this:
   ```sudo apt-get install
   sudo apt-get upgrade```
   ```

   ##### *Strict MD*

   ````
   1.  Install Linux
   2.  Enter this:
       ```
       sudo apt-get install
       sudo apt-get upgrade
       ```
   ````

---

### PR -> Build -> Merge -> Publish

Whenever a PR is made, Netlify automatically builds it and serves a preview. In case the build doesn't pass(red X), then add a ninja commit to fix it.
