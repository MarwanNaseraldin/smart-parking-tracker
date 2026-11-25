FROM httpd:2.4-alpine

# יצירת תיקיית תמונות בנתיב ברירת המחדל של Apache
RUN mkdir -p /usr/local/apache2/htdocs/images

# העתקת התמונות לתוך האימג'
COPY images/ /usr/local/apache2/htdocs/images/

EXPOSE 80