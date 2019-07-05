# About
Modern and clean CV that uses CircleCI to build itself and publish to GitHub pages.

# Setup
1. Fork this repo.
2. Generate SSH key pair `ssh-keygen -m PEM -t rsa -C "your@email.com" -f /tmp/deploy_key -q -N ""`.
3. Go to repo settings on GitHub:
    - Go to `Deploy keys` and add the newly created public key (`cat /tmp/deploy\_key.pub`). Be sure to check the `Allow write access` checkbox.
4. Log-in to CircleCI:
    - In `ADD PROJECTS` tab select your repo and enable builds.
    - Go to project settings, `SSH Permisions` and add the private key (`cat /tmp/deploy\_key`) and set the `Hostname` to `github.com`, take note of the fingerprint.
6. Update settings in `.circleci/config.yml`.
7. Push the changes.
9. Each time you push to the master branch your compiled CV will be pushed to gh-pages branch and be avilable at https://username.github.io/CV/cv.pdf.

# License

Copyright (C) 2019, Maciej Mucha  
Copyright (C) 2015, Edgar Klenske  
Copyright (C) 2014, Jelmer Tiete  
Copyright (C) 2012, Adrien Friggeri

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
