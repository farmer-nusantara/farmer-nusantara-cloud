# App Engine
Quickstart guide to deploy Apps on App Engine
1. Set App Engine Region, Create.
2. Open Editor, and clone the code from your repository using `git clone https://github.com/farmer-nusantara/farmer-nusantara-api.git`.
3. Move into your repository path using `cd farmer-nusantara-api`.
4. Create app.yaml on your folder.
5. Set app.yaml configuration 
   ```runtime: nodejs
      env: flex 
      service: default
      instance_class: F2
      automatic_scaling:
        min_num_instances: 1
        max_num_instances: 5
      env_variables:
        GCLOUD_STORAGE_BUCKET: farmer-nusantara-images-storage
6. Rename .env.example to .env.
7. Type the command `npm install` on your terminal, to install all the required libraries.
8. After that, you can type the command `npm start` or `npm run dev` to test before deploy.
9. After all done, then the code ready to deploy.
10. Type `gcloud app deploy` on terminal, then type Y to prompt.
11. After deploy success, type `gcloud app browse` to see your App Engine URL.
