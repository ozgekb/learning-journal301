- Today I learned that I can change position of object by using jquery function.
- Using sprite-sheet help us to load 1 image and using  diffrent position of it .
$(document).ready(function(){
  $('.checkbox1').click(function(){
    $('.checkbox1').css('width','50px');
    $('.checkbox1').css('height','50px');
    $('.checkbox1').css('background-position','-102px','-70px');
    $('.checkbox1').css('margin-left','2%');
    $('.checkbox2').css('width','50px');
    $('.checkbox2').css('height','50px');
    $('.checkbox2').css('background-position','-40px','-70px');
    $('.checkbox2').css('margin-left','2%');
  });
  $('.checkbox2').click(function(){
    $('.checkbox2').css('width','50px');
    $('.checkbox2').css('height','50px');
    $('.checkbox2').css('background-position','-102px','-70px');
    $('.checkbox2').css('margin-left','2%');
    $('.checkbox1').css('width','50px');
    $('.checkbox1').css('height','50px');
    $('.checkbox1').css('background-position','-40px','-70px');
    $('.checkbox1').css('margin-left','2%');
  });

-  We use double-quote while using camelcase for sql statement.

  function queryThree(author_id) {
    client.query(
      `INSERT INTO articles (author_id, title, category, "publishedOn", body) VALUES ($1, $2, $3, $4, $5)`,
      [author_id, request.body.title, request.body.category, request.body.publishedOn, request.body.body],
      function(err) {
        if (err) console.error(err);
        response.send('insert complete');
      }
    );
  }
});
