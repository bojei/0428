# 0428
var game = new Phaser.Game(400, 400, Phaser.AUTO, "game",
    { preload: preload, create: create, update: update });
    game.load.crossOrigin = 'anonymous';
game.load.baseURL = 'http://s.ntustcoding.club/ns-shaft-workshop/';
game.load.spritesheet('player', 'player.png', 32, 32);
game.load.spritesheet('player', '/assets/player.png', 32, 48);
game.load.image('normal', '/assets/block.png');
player = game.add.sprite(200, 200, 'player');
player = game.add.sprite(200, 200, 'player');
game.physics.arcade.enable(player);
var x = player.body.x;
var y = player.body.y;
// 印出 x,y
console.log(x, y);
player.body.x = 100;
player.body.y = 100;
player.body.x += 1;
player.body.velocity.x = 60;
keyboard = game.input.keyboard.addKeys({
    'up': Phaser.Keyboard.UP,
    'down': Phaser.Keyboard.DOWN,
    'left': Phaser.Keyboard.LEFT,
    'right': Phaser.Keyboard.RIGHT
});
if(keyboard.left.isDown) {
	// 當左方向鍵按下時執行的動作...
}
if(keyboard.right.isDown) {
	// 當右方向鍵按下時執行的動作...
}
game.load.spritesheet('player', 'player.png', 32, 32);
player.animations.add('left', [0, 1, 2, 3], 6);
player.animations.add('right', [9, 10, 11, 12], 6);
player.animations.play('right');
player.frame = 1;
var a = 10;

function test1 () {
    var a = 100;
    console.log(a);
}

function test2 () {
    console.log(a);
}

test1(); // 印出 100
text2(); // 印出 10
var player;
var keyboard;

create() {
    player = game.add.sprite(200, 200, 'player');
    keyboard = game.input.keyboard.addKeys({
        'left': Phaser.Keyboard.LEFT,
        'right': Phaser.Keyboard.RIGHT
    });
}

update() {
    if(keyboard.left.isDown) {
        player.body.velocity.x = -250;
    }
    if(keyboard.right.isDown) {
        player.body.velocity.x = 250;
    }
}
leftWall = game.add.sprite(0, 0, 'wall');
game.physics.arcade.enable(leftWall);
// 設定固定屬性
leftWall.body.immovable = true;
game.physics.arcade.collide(player, [leftWall, rightWall]);
player.body.velocity.y += 30;
player.body.gravity.y = 500;
// 存有 5 個成績的陣列
var scores = [100, 95, 90, 85, 80];

console.log(scores[2]); // 取出第0個成績，印出 90

// 把第0個的成績改成 60
scores[0] = 60;
console.log(scores[0]); // 取出第0個成績，印出 60

// 新增新的成績
scores.push(90);
console.log(scores[5]); // 取得第5個成績，印出 90

// 取得成績的個數
console.log(scores.length); // 印出 6
var platforms = [];

function create() {
    var platform = game.add.sprite(0, 0, 'normal');
    platforms.push(platform);
}
var now = Phaser.time.now;
console.log(now); // 印出遊戲開始到現在的時間
platform.destroy();
platforms.splice(i, 1);
// rand 是0~100的隨機數字
var rand = Math.random()*100;
game.physics.arcade.collide(player, platforms, effect);
function effect(player, platform) {
    console.log(platform.key);
}
platform.animations.add('scroll', [0, 1, 2, 3], 16, true);
var pikachu = {
    color: "yellow",
    weight: 13.2,
    height: 40,
    gender: true
}
// 印出 13.2公分
console.log(pikachu.height + "公分");

// 皮卡丘增胖 5 公斤
pikachu.weight += 5;
var pikachu = {}

pikachu.color = "yellow";
pikachu.weight = 13.2;
pikachu.height = 40;
pikachu.gender = true;
player.life = 10;
player.touchOn = undefined;
player.unbeatableTime = 0;
text = game.add.text(10, 10, "");
text.setText("這裡放新的文字");
game.physics.arcade.enable(platform);
platform.body.setSize(96, 15, 0, 15);
platform.body.checkCollision.down = false;
platform.body.checkCollision.left = false;
platform.body.checkCollision.right = false;
setTimeout(function() {
    // do something...
}, 100);
game.camera.flash(0xff0000, 100);


小朋友下樓梯參考網站:https://hackmd.io/p/rkR_9r4Qe#/
