

# Project: Movie and Tv-shows streaming service

## FrontEnd Layout
* Homepage

![This is an image](https://github.com/Patrick-BP/CS566-FinalPoject/blob/main/img/homepage.png)

* Admin
![This is an image](https://github.com/Patrick-BP/CS566-FinalPoject/blob/main/img/admin.png)

* Movie Details
![This is an image](https://github.com/Patrick-BP/CS566-FinalPoject/blob/main/img/movieDetails.png)

* Tv-Show Details 
![This is an image](https://github.com/Patrick-BP/CS566-FinalPoject/blob/main/img/tvshowDetails.png)

## BackEnd 
* authRoute
  - post('/user/login', authController.login)
  
* userRoute
  - post('/signup', userController.saveUser)
  - patch('/:id', userController.updateOneUser)
  - router.delete('/del/:id', userController.deleteOneUser)
  - patch('/changepassword/:id', userController.changePassword)
  - patch('/pic/:userId',storage, userController.uploadProfilePic)
  - get('/:id',userController.getOneUser)

* usersRoute
  - get('/', userController.getAllUsers)
  - get('/:id',userController.getOneUser)
  - patch('/:id', userController.updateOneUser)
  - delete('/del/:id', userController.deleteOneUser)
 
* tvshowRoute
  - get('/', TvshowsController.getAll)
  - post('/', TvshowsController.save)
  - get('/:tvId', TvshowsController.getById)
  - delete('/del/:tvId', TvshowsController.delById)
  - patch('/:tvId', TvshowsController.updateById)
  - patch('/poster/:tvId',storage, TvshowsController.updatePosterById)


* MoviesRoute
  - get('/:movieId', MovieController.getById)
  - get('/', MovieController.getAll)

* MovieRoute
  - get('/', MovieController.getAll)
  - post('/', MovieController.save)
  - get('/:movieId', MovieController.getById)
  - delete('/del/:movieId', MovieController.delById)
  - patch('/:movieId', MovieController.updateById)
  - patch('/poster/:movieId',storage, MovieController.updatePosterById)
  - patch('/video/:movieId',storageVideo, MovieController.updateVideoById)
  
* PlayListRoute
  - get('/:userId', playListController.getAll)
  - delete('/:playlistId', playListController.delById)
  - post('/add', playListController.save)
  
* episodeRoute
  - get('/', episodeController.getAll)
  - post('/', episodeController.save)
  - get('/:episId', episodeController.getEpisodesTvshowById)
  - delete('/del/:episId', episodeController.delById)
  - patch('/video/:episId',storageVideo, episodeController.updateVideoById)

* commnentsRoute
  - get('/:movieId', CommentsController.getAllComnts)
  - post('/add', CommentsController.save)
  - get('/:commentId', CommentsController.getById)
  - delete('/:commentId', CommentsController.delById)
  - put('/:commentId', CommentsController.updateById)

## Database
* Users
* Movies
* Tv-shows
* Episodes
* Comments
* Replies
* PlayList
