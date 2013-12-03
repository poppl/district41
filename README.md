Users/                                                                                              000755  000765  000024  00000000000 12247445306 012735  5                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         Users/janarde/                                                                                      000755  000765  000024  00000000000 12247445306 014341  5                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         Users/janarde/Documents/                                                                            000700  000765  000024  00000000000 12247445306 016270  5                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         Users/janarde/Documents/Work/                                                                       000755  000765  000024  00000000000 12247445306 017224  5                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         Users/janarde/Documents/Work/District41/                                                            000755  000765  000024  00000000000 12247445306 021156  5                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         Users/janarde/Documents/Work/District41/content.js                                                  000644  000765  000024  00000000567 12247445306 023176  0                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         var viewModel = {
    topics : ko.observableArray(['What is District 41?', 'When is the District 41 meeting?', 'Where is the District 41 meeting?', 'Why is District 41 valuable to AA members?', 'How is District 41 serving the AA primary purpose?', 'Who is involved in District 41?']),
    selectedTopic : ko.observable("What is District 41?")
};
ko.applyBindings(viewModel);
                                                                                                                                         Users/janarde/Documents/Work/District41/contentController.js                                        000644  000765  000024  00000005631 12247445306 025237  0                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         function contentController() {
    var what = { question: "What is District 41?",
                 answer : "<p>District 41 is a service entity of Alcoholics Anonymous. We represent and serve AA members in Magnolia, Queen Anne, and South Lake Union of Seattle Washington.</p>"
    };

    var when = { question: "When is the District 41 meeting?",
                 answer: "<p>We meet the second Wednesday of every month from 6:00pm - 7:30pm.</p>"
    };

    var where = { question: "Where is the District 41 meeting?",
                  answer: "<p>Denny Park Lutheran Church<br>766 John Street<br>Seattle, WA. 98109</p>"
    };

    var why = { question: "Why is District 41 valuable to AA members?",
                answer: "<p>When AA group-elected General Service Representatives (GSRs) share information about their groups at the District meeting, we are able to help each other develop unity within the Fellowship. Also, we forward your group conscience to the Area Delegate, who attends the annual AA General Service Conference and votes on major proposals that affect the entire AA Fellowship. District 41 is your link to having a voice in Alcoholics Anonymous as a whole.</p>"
    };

    var how = { question: "How is District 41 serving the AA primary purpose?",
                answer: "<p>Our purpose is to carry the AA message to the alcoholic who still suffers. District 41 assists groups and members in serving this purpose. We work through committees to reach alcoholics outside of our meetings: jails and other correctional facilities, treatment centers, professionals who encounter alcoholics, and the public.</p>"
    };

    var who = { question: "Who is involved in District 41?",
                answer: "<p>In addition to group-elected GSRs, the District Committee is made up of officers and standing committee chairs. Our officers are trusted servants elected by the GSRs; they are responsible to the groups and do not govern. Beyond the District Committee, AA members from all over Seattle are involved in our various service committees. District 41 has a place for any alcoholic who is interested in service. <br><h3>District Committee Officers:</h3><br><div class='content'><ul class='bullet-list'><li> GSRs</li><li> Alt. GSRs</li><li>DCM</li><li> Alt. DCM</li><li> Treasurer</li><li>Secretary</li></ul></div><br><h3> District Committee Chairs:</h3><br><div class='content'><ul class='bullet-list'><li>Accessibility</li><li>Archives</li><li>Cooperation with Professional Community (CPC)</li><li>Corrections </li><li>Grapevine & Literature</li><li>Public Information (PI)</li><li>Treatment</li><li>Web</li><li>Intergroup Liaison</li></ul></div><p>"
    };

    var that = this;
    $(document).ready(function() {
        $("#district-info").hide();
        $('.dropdown-toggle').dropdown();
        $("#info-btn-close").click(function() {
            $("#district-info").hide();
        });
    });    
}

var cc = new contentController();
                                                                                                       Users/janarde/Documents/Work/District41/index.html                                                  000644  000765  000024  00000005074 12247445306 023161  0                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         <!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" >
<head>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
    <link rel="stylesheet" type="text/css" href="dist/css/bootstrap.min.css">
    <title>District 41</title>
</head>
<body>
  <div class="banner">
    <h1>Welcome to district 41 AA</h1>
  </div>
  <div class="my-dropdown content"> 
      <p><h3 class="heading">About District 41</h3></p>
      <button id="topic-dropdown" type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown">
        Frequently Asked Questions<span class="caret"></span>
      </button>
      <ul id="dropdown-list" class="dropdown-menu dropdown" role="menu" data-bind="foreach: topics">
        <li><a href="#" data-bind="text: $data"></a></li>
      </ul>
  </div>
  <div id="district-info"class="topic alert alert-info alert-dismissable">
    <button id="info-btn-close" type="button" class="close" data-dismiss="alert" aria-hidden="true">&times;</button>
    <span id="answer"></span>
  </div>
  <div id="preamble" class="content">
    <p id="main">Alcoholics Anonymous is a fellowship of men and women who share their experience, strength and hope with each other that they may solve their common problem and help others to recover from alcoholism. The only requirement for membership is a desire to stop drinking. There are no dues or fees for AA membership; we are self-supporting through our own contributions. AA is not allied with any sect, denomination, politics, organization or institution; does not wish to engage in any controversy; neither endorses nor opposes any causes. Our primary purpose is to stay sober and help other alcoholics to achieve sobriety.
    </p>
  </div>
  <div id="schedule" class="content">
    <a id="link" href="http://schedule.area72aa.org/meetings/schedule.php?function=district&district=41">Click here for a schedule of District 41 meetings.</a>
  </div>
  <div id="blurb" class="content">
    <p id="main">The web committee would appreciate your feedback. Please take a moment to complete the survey at the link below so that we may better serve the needs of our district.</p>
    <a id="link" href="http://www.surveymonkey.com/s/QPKVT7N">Click here to take survey</a>
  </div>
  <script type='text/javascript' src='dist/js/jquery-1.10.2.min.js'></script>
  <script type='text/javascript' src='dist/js/knockout-3.0.0.js'></script> 
  <script type='text/javascript' src='content.js'></script>
  <script type='text/javascript' src='dist/js/bootstrap.min.js'</script>
  <script type='text/javascript' src='contentController.js'></script>  

</body>
</html>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                    Users/janarde/Documents/Work/District41/mystyle.css                                                 000644  000765  000024  00000002262 12247445306 023400  0                                                                                                    ustar 00janarde                         staff                           000000  000000                                                                                                                                                                         hr
{
  color:sienna;
}
.banner
{
  padding:100px;
}

h1
{
  text-align:center;
  #text-shadow: 2px 0px #888888;
  font-family:"Lucida Console", Monaco, monospace;
  font-size:2.5em;
  position:relative;
}

.heading
{
    text-align:center;
    position:relative;
    font-family:"Lucida Console", Monaco, monospace;
    color:#6699FF;
}
.content
{
  padding:10px;
  text-align:center;
  #border:2px solid #a1a1a1;
  #border-radius:50px;
  #box-shadow: 5px 5px 2px #888888;
  margin:10px
}

.bullet-list
{
    text-align:left;
}

#dropdown-list
{
    margin:0 auto;
    position: relative;
    text-align: right;
}

.my-dropdown
{
    margin:0 auto;
    position: relative;
    text-align: center;
}
.topic
{
  visibility:hidden;
  text-align:center;
  font-family:"Lucida Console", Monaco, monospace;
  font-size:1em;
}

#main 
{
  text-align:center;
  font-family:"Lucida Console", Monaco, monospace;
  font-size:1em;
  position:relative;
}

#link
{
  font-family:"Lucida Console", Monaco, monospace;
  font-size:1.25em;
  position:relative;
}

#answer
{
    display:block;
}

body 
{
  background-image:url('img/background-fade.jpg');
  background-repeat:no-repeat;
  background-position:left top;
}
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              