This config is an attempt to manage staging push vs production push by using Terraform workspaces (staging, production). This doesn't work well because you end up with the Terraform state for the same backend resource (the Property Manager config) being held in 2 places. This means that Terraform will get confused.