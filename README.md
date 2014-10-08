Script

$(document).ready(function(){
  $('.user-head').click(function(){
    $('.user-box').slideToggle('slow');
  });

  $('.close').click(function(){
    $('.msg_box').hide('slow');
  });

  $('.username').click(function(){
    $('.msg_box').show('slow');
  });

  $('textarea').keypress(function(e){
    if(e.keyCode == 13){
      var msg = $(this).val();
      $(this).val('');
      $("<div class='msg_b'>"+msg+"</div>").insertBefore('.msg_insert');
      $('.msg_box_body').scrollTop($('.msg_box_body')[0].scrollHeight);
          }
  });

});

