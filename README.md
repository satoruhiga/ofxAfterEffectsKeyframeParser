### usage

	ofxAfterEffectsKeyframeParser aekey;
	aekey.open("test.txt");
	
	aekey.dumpTrackName();
	
	const ofxAfterEffectsKeyframeParser::Track &t = aekey.getTrack("Motion Trackers/Tracker #1/Track Point #1/Attach Point");
	
	for (int i = 0 ; i <= aekey.getLastFrame(); i++)
	{
		cout << i << " " << t.getParam(i, "X pixels") << endl;
	}
