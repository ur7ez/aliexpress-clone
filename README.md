# AliExpress Clone / (aliexpress-clone)

_Build with help and inspiration of tutorial video by [JOHN WEEKS DEV](https://youtu.be/dVcCRFVhz74?si=iGO8OsTB8LRvrUBD)_

If you'd like a step-by-step guide on how to build this and other projects check out this awesome [YouTube channel](https://www.youtube.com/@johnweeksdev).

## App Setup (localhost)

git clone this project
```
cp .env.example .env

npm i

npx prisma generate

npm run dev
```

You'll have to setup a Supabase account & Stripe account, then add all the details in to your .env file.

Once you've connected your application to Supabase. You'll also need to setup the Auth Providers:
[Google](https://cloud.google.com) and 
[Github](https://github.com/settings/developers)

    https://supabase.com/docs/guides/auth/social-login/auth-google
    https://supabase.com/docs/guides/auth/social-login/auth-github

Now run the command to migrate your database tables and run your seed file.

```
npx prisma migrate dev --name init
```