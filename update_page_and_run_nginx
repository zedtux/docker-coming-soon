#!/usr/bin/env bash

echo 'Updating the index.html file ...'
echo ''

# Page title
if [[ -z "$TITLE" ]]
then
  echo "WARNING: No TITLE given, using the default one"
  TITLE='Coming soon ...'
fi;
echo "Updating title to $TITLE ..."
sed -i "s/ENV_TITLE/$TITLE/" "$BASE_DIR/index.html"

# Product name
if [[ -z "$PRODUCT_NAME" ]]
then
  echo "WARNING: No PRODUCT_NAME given, using the default one"
  PRODUCT_NAME='Sssonn'
fi;
echo "Updating the product name with $PRODUCT_NAME ..."
sed -i "s/ENV_PRODUCT_NAME/$PRODUCT_NAME/" "$BASE_DIR/index.html"

# Catchy phrase
if [[ -z "$CATCHY_PHRASE" ]]
then
  echo "WARNING: No CATCHY_PHRASE given, using the default one"
  CATCHY_PHRASE='Find the best Bootstrap 3 freebies and themes on the web.'
fi;
echo "Updating the catchy phrase with $CATCHY_PHRASE ..."
sed -i "s/ENV_CATCHY_PHRASE/$CATCHY_PHRASE/" "$BASE_DIR/index.html"

# Facebook button
if [[ -z "$FACEBOOK_URL" ]]
then
  echo "WARNING: No Facebook URL given, removing the button."
  FACEBOOK_BUTTON=''
  echo "Removing the Facebook button ..."
else
  FACEBOOK_BUTTON="<li><a href=\"$FACEBOOK_URL\"><i class=\"fa fa-facebook-square\"></i> Share</a></li>"
  echo "Updating the Facebook button ..."
fi;
sed -i "s~ENV_FACEBOOK_BUTTON~$FACEBOOK_BUTTON~" "$BASE_DIR/index.html"

# Twitter button
if [[ -z "$TWITTER_URL" ]]
then
  echo "WARNING: No Twitter URL given, removing the button."
  TWITTER_BUTTON=''
  echo "Removing the Twitter button ..."
else
  TWITTER_BUTTON="<li><a href=\"$TWITTER_URL\"><i class=\"fa fa-twitter\"></i> Tweet</a></li>"
  echo "Updating the Twitter button ..."
fi;
sed -i "s~ENV_TWITTER_BUTTON~$TWITTER_BUTTON~" "$BASE_DIR/index.html"

# Github button
if [[ -z "$GITHUB_URL" ]]
then
  echo "WARNING: No Github URL given, removing the button."
  GITHUB_BUTTON=''
  echo "Removing the Github button ..."
else
  GITHUB_BUTTON="<li><a href=\"$GITHUB_URL\"><i class=\"fa fa-github\"></i> Follow</a></li>"
  echo "Updating the Github button ..."
fi;
sed -i "s~ENV_GITHUB_BUTTON~$GITHUB_BUTTON~" "$BASE_DIR/index.html"

# Email button
if [[ -z "$EMAIL" ]]
then
  echo "WARNING: No Email address given, removing the button."
  EMAIL_BUTTON=''
  echo "Remving the Email button ..."
else
  EMAIL_BUTTON="<li><a href=\"mailto:$EMAIL\"><i class=\"fa fa-envelope-o\"></i> Email</a></li>"
  echo "Updating the Email button ..."
fi;
sed -i "s~ENV_EMAIL_BUTTON~$EMAIL_BUTTON~" "$BASE_DIR/index.html"

echo "Starting Nginx ..."
nginx -g "daemon off;"
