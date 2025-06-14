REPO_NAME="opay-backend"
if gh repo view $REPO_NAME > /dev/null 2>&1; then
echo "ℹ️ Repository '$REPO_NAME' already exists on GitHub."
else
echo "📦 Creating GitHub repo: $REPO_NAME"
gh repo create $REPO_NAME --public --source=. --push
fi