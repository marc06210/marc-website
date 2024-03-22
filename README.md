docker build -t declicimmo .

docker run -p 80:80 declicimmo


pour pousser un fichier
exemple on pousse photo.jpeg dans le path complet
scp -P 38853 photo.jpeg declicimmo@2.15.249.172:/home/declicimmo/www/html/christophe/photo.jpeg