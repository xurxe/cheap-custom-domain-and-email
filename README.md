# Custom domain and email - on the cheap!

- This is mostly a cheatsheet for myself, but maybe someone else can find it useful!
- There's no files, all the info is here on README.md :)

## Cost

- Domain: it varies, but a .com domain from domain.com is usually 9.99 USD for a year (+ optional 8.99 USD for privacy protection)
- Hosting: free with GitHub pages
- Email: free with a combination of domain.com and mail.google.com
- The tools below: free

## Tools

- Gmail account
- GitHub account
- Domain.com account
- Virtual Studio Code (VSC)

## Buy domain

1. Go to domain.com
2. Search for your domain. For example: xurxe-example.com
    - If it's available, it will be added to your cart.
    - It automatically selects 2 years of domain purchase and 2 years of privacy protection, which quickly ramps up the price. I switch it to 1 year and keep the privacy protection on
3. Click Continue. DO NOT choose any add-ons
4. Click Proceed to Billing. After that it's pretty standard stuff
    - If you have an account, log in
    - If you don't, create a new account
5. Follow the instructions you will receive by email

## Create local repository

1. Create folder in your computer. For example: xurxe-example
2. Open VSC
3. Go to File > Open > xurxe-example
4. Create some files (I like to copy from my [Web project template repository](https://github.com/xurxe/web-project-template)).
5. Go to Terminal > New terminal
6. Initialize: `git init`
7. Add: `git add`
8. Commit: `git commit -m "Created project"` (for example)

## Create GitHub repository

1. Go to GitHub > Repositories > New
2. Give it the same name as your local repository. For example: xurxe-example
3. Click create
4. Copy the code that looks like this:
    `git remote add origin https://github.com/xurxe/xurxe-example.git`
    `git push -u origin master`
5. Go back to VSC and paste that code into your terminal

## Create GitHub pages

1. Go to GitHub > Repositories > xurxe-example > Settings > GitHub pages
2. From the dropdown menu, choose "master branch"
3. In Custom domain, enter your domain. For example: xurxe-example.com
    - This will create a file called CNAME. Don't delete it!
    
## Redirect domain

1. Go to Domain.com > Login
2. Find your domain and click on Manage > DNS & Nameservers
3. Locate the first line, which shows: `Record: A; Name: @; Content: 66.96.162.135`
    - Click on the three dots > Edit
    - Change `66.96.162.135` to `185.199.108.153`
4. Locate the second line, which shows: `Record: A; Name: ftp; Content: 66.96.162.135`
    - Click on the three dots > Edit
    - Change `66.96.162.135` to `185.199.108.153`
5. Locate the line that shows: `Record: A; Name: *; Content: 66.96.162.135`
    - Click on the three dots > Edit
    - Change `66.96.162.135` to `185.199.108.153`
6. Scroll up and click on Add DNS Record. Add the following record:
    - `Name: @; Record: A; Content: 185.199.109.153`
    - Click Add DNS
7. Repeat step 6 to add the following records:
    - `Name: @; Record: A; Content: 185.199.110.153`
    - `Name: @; Record: A; Content: 185.199.111.153`
    - `Name: www; Record: CNAME; Content: xurxe.github.io` (substitute my GitHub username with yours)
    
## Create custom email address

Coming soon.
    
## Author

Xurxe Toivo García

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- All the people who have written articles and tutorials on how to do this
- Customer support techs from domain.com
