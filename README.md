# Jenkins CI/CD Assignment

This project demonstrates setting up a CI/CD pipeline using Jenkins with a master-slave architecture, including staging and production deployments.

## 🚀 Features
- Git-based source control
- Jenkins master-agent setup
- Jenkins Pipeline with Build, Test, Deploy
- Failure handling
- PR handling
- Multi-branch support
- Staging & Production environments

## 🏗️ Pipeline Stages
1. **Build** - Compiles the Python app
2. **Test** - Placeholder for unit tests
3. **Deploy to Staging** - Copies to /deploy/staging
4. **Deploy to Production** - Conditional on main branch + manual input

## 🧪 Running Locally
```bash
pip install -r requirements.txt
python app.py
```

## 🖥️ Jenkins Setup Summary
- Install Jenkins and required plugins
- Create admin user and roles
- Setup agent node
- Create Pipeline project using `Jenkinsfile`
- Configure GitHub Webhooks for PRs and pushes

## 📈 Benefits of CI/CD
- Faster feedback
- Automated testing & deployment
- Consistent environments
- Improved collaboration
- Reduced manual errors