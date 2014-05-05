#include "SFApp.h"

SFApp::SFApp() : is_running(true) {

  surface = SDL_GetVideoSurface();
  app_box = make_shared<SFBoundingBox>(Vector2(surface->w/2, surface->h/2), surface->w/2, surface->h/2);
  player  = make_shared<SFAsset>(SFASSET_PLAYER);
  auto player_pos = Point2(surface->w/2, 100.0f);
  player->SetPosition(player_pos);

  // This is the positioning of the walls in the level. Starting from the top left corner 0:0
  // 1st Row (from top left)
  auto wall = make_shared<SFAsset>(SFASSET_WALL);
  auto pos   = Point2(50.0f, 750.0f);   // 1st wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(150.0f, 750.0f);		// 2nd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(250.0f, 750.0f);		// 3rd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(450.0f, 750.0f);		// 4th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(550.0f, 750.0f);		// 5th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(650.0f, 750.0f);		// 6th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  // 2nd Row
  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(50.0f, 650.0f);		// 1st wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(650.0f, 650.0f);		// 2nd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  // 3rd Row
  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(50.0f, 550.0f);		// 1st wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(250.0f, 550.0f);		// 2nd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(350.0f, 550.0f);		// 3rd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(450.0f, 550.0f);		// 4th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(650.0f, 550.0f);		// 5th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  /*********************************************************/
  /********** There are no walls in the 4th Row ************/
  /*********************************************************/

  // 5th Row
  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(50.0f, 350.0f);		// 1st wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(250.0f, 350.0f);		// 2nd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(350.0f, 350.0f);		// 3rd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(450.0f, 350.0f);		// 4th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(650.0f, 350.0f);		// 5th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  // 6th Row
  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(50.0f, 250.0f);		// 1st wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(650.0f, 250.0f);		// 1st wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  // 7th Row
  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(50.0f, 150.0f);		// 1st wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(150.0f, 150.0f);		// 2nd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(250.0f, 150.0f);		// 3rd wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(450.0f, 150.0f);		// 4th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(550.0f, 150.0f);		// 5th wall
  wall->SetPosition(pos);
  walls.push_back(wall);

  wall = make_shared<SFAsset>(SFASSET_WALL);
  pos   = Point2(650.0f, 150.0f);		// 6th wall
  wall->SetPosition(pos);
  walls.push_back(wall);  

  // This is the positioning of the food in the level. Starting from the top left corner 0:0
  // 1st Row (from top left)
  auto food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(150.0f, 650.0f);	// 1st food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(250.0f, 650.0f);	// 2nd food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(350.0f, 650.0f);	// 3rd food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(450.0f, 650.0f);	// 4th food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(550.0f, 650.0f);	// 5th food
  food->SetPosition(pos);
  foods.push_back(food);

  // 2nd Row
  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(150.0f, 550.0f);	// 1st food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(550.0f, 550.0f);	// 2nd food
  food->SetPosition(pos);
  foods.push_back(food);

  // 3rd Row
  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(150.0f, 450.0f);	// 1st food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(250.0f, 450.0f);	// 2nd food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_CHERRY);
  pos  = Point2(350.0f, 450.0f);	// 3rd food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(450.0f, 450.0f);	// 4th food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(550.0f, 450.0f);	// 5th food
  food->SetPosition(pos);
  foods.push_back(food);

  // 4th Row
  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(150.0f, 350.0f);	// 1st food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(550.0f, 350.0f);	// 2nd food
  food->SetPosition(pos);
  foods.push_back(food);

  // 5th Row
  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(150.0f, 250.0f);	// 1st food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(250.0f, 250.0f);	// 2nd food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(350.0f, 250.0f);	// 3rd food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(450.0f, 250.0f);	// 4th food
  food->SetPosition(pos);
  foods.push_back(food);

  food = make_shared<SFAsset>(SFASSET_FOOD);
  pos  = Point2(550.0f, 250.0f);	// 5th food
  food->SetPosition(pos);
  foods.push_back(food);
	
}	

SFApp::~SFApp() {
}

/**
 * Handle all events that come from SDL.
 * These are timer or keyboard events.
 */
void SFApp::OnEvent(SFEvent& event) {
  SFEVENT the_event = event.GetCode();  
  switch (the_event) {
  case SFEVENT_QUIT:
    is_running = false;
    break;
  case SFEVENT_UPDATE:
    OnUpdateWorld();
    OnRender();
    break;
  case SFEVENT_PLAYER_LEFT_KEYUP:
    player->movingLeft = false;
    break;
  case SFEVENT_PLAYER_RIGHT_KEYUP:
    player->movingRight = false;
    break;
  case SFEVENT_PLAYER_UP_KEYUP:
    player->movingUp = false;
    break;
  case SFEVENT_PLAYER_DOWN_KEYUP:
    player->movingDown = false;
    break;
  case SFEVENT_PLAYER_LEFT_KEYDOWN:
    player->movingLeft = true;
    break;
  case SFEVENT_PLAYER_RIGHT_KEYDOWN:
    player->movingRight = true;
    break;
  case SFEVENT_PLAYER_UP_KEYDOWN:
    player->movingUp = true;
    break;
  case SFEVENT_PLAYER_DOWN_KEYDOWN:
    player->movingDown = true;
    break;
  }
}

int SFApp::OnExecute() {
  // Execute the app
  SDL_Event event;
  while (SDL_WaitEvent(&event) && is_running) {
    // if this is an update event, then handle it in SFApp,
    // otherwise punt it to the SFEventDispacher.
    SFEvent sfevent((const SDL_Event) event);
    OnEvent(sfevent);
  }
}

void SFApp::OnUpdateWorld() {
  
  // Detect collision with wall
  for(auto w : walls) {
    if(player->CollidesWith(w)) {
        if (player-> movingLeft) {
          player->GoEast();
          player->movingLeft = false;
        }
        
        if (player-> movingRight) {
          player->GoWest();
          player->movingRight = false;
        }

        if (player-> movingUp) {
          player->GoSouth();
          player->movingUp = false;
        }

        if (player-> movingDown) {
          player->GoNorth();
          player->movingDown = false;
        }
  	}
  }

  // Detect collisions with food
  for(auto f : foods) {        
      if(player->CollidesWith(f)) {
        f->HandleCollision();
  	}
  }

  // remove dead walls (the long way)
  list<shared_ptr<SFAsset>> tmp;
  for(auto f : foods) {
    if(f->IsAlive()) {
      tmp.push_back(f);
    }
  }
  foods.clear();
  foods = list<shared_ptr<SFAsset>>(tmp);

  if (player->movingUp == true) {
      player->GoNorth();
  }

  if (player->movingDown == true) {
      player->GoSouth();
  }

  if (player->movingLeft == true) {
      player->GoWest();
  }

  if (player->movingRight == true) {
      player->GoEast();
  }

}

void SFApp::OnRender() {
  // clear the surface
  SDL_FillRect(surface, NULL, SDL_MapRGB(surface->format, 122, 65, 65) );

  // draw the player
  player->OnRender(surface);

  for(auto c: cherry) {
    if(c->IsAlive()) {c->OnRender(surface);}
  }

  for(auto w: walls) {
    if(w->IsAlive()) {w->OnRender(surface);}
  }

  for(auto f: foods) {
    f->OnRender(surface);
  }

  // Switch the off-screen buffer to be on-screen
  SDL_Flip(surface);
}

void SFApp::cherryPos() {
  auto pb = make_shared<SFAsset>(SFASSET_CHERRY);
  auto v  = player->GetPosition();
  pb->SetPosition(v);
  cherry.push_back(pb);
}
