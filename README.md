https://www.sejuku.net/blog/28967#ajax-3

【Rails入門】ajaxの使い方まとめ（学習メモ）

今回の学習ポイント

app/views/practice/index.html.erb

:remote => trueの部分です。こう記述することによってturbolinkを有効にできる。
Railsではturbolinkを使えば、ajaxが自動的に使えるようになる。

[app/controllers/practice_controller.rbのindexアクションの内容]
indexでポストされたデータをparams[:title]で受け取った後、respond_toメソッドを使って結果をどのフォーマットで返すかを指定しています。

routes.rbに
resources :hoge
とすることでこれでRESTfulなリソースの振り分けができます。

内容{
    
    振り分けの内容

    GET	  
    /photos  
    photos#index  
    すべての写真の一覧を表示  

    GET	    
    /photos/new	 
    photos#new	   
    写真を1つ作成するためのHTMLフォームを返す    

    POST	   
    /photos	  
    photos#create	 
    写真を1つ作成する  

    GET	      
    /photos/:id  	    
    photos#show	 
    特定の写真を表示する  

    GET	    
    /photos/:id/edit  
    photos#edit	 
    写真編集用のHTMLフォームを1つ返す  

    PATCH/PUT	 
    /photos/:id	    
    photos#update	 
    特定の写真を更新する  

    DELETE	 
    /photos/:id	   
    photos#destroy 	
    特定の写真を削除する   
}
