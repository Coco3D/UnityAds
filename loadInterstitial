using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.Advertisements;
public class loadInterstitial : MonoBehaviour, IUnityAdsLoadListener, IUnityAdsShowListener
{
    public string androidAdUnitId;
    public string iosAdUnitId;

    string adUnitId;

    void Awake() {
#if UNITY_IOS
        adUnitId = iosAdUnitId;
#elif UNITY_ANDROID
        adUnitId = androidAdUnitId;
#endif

    }

    public void LoadAd() {
        print("Loading interstitial!!");
        Advertisement.Load(adUnitId, this);
    }

    public void OnUnityAdsAdLoaded(string placementId)
    {
        print("interstitial loaded!!");
        ShowAd();
    }

    public void OnUnityAdsFailedToLoad(string placementId, UnityAdsLoadError error, string message)
    {
        print("interstitial failed to load");
    }



    public void ShowAd() {
        print("showing ad!!");
        Advertisement.Show(adUnitId, this);
    }

    public void OnUnityAdsShowClick(string placementId)
    {
        print("interstitial clicked");
    }

    public void OnUnityAdsShowComplete(string placementId, UnityAdsShowCompletionState showCompletionState)
    {
        print("interstitial show complete");

    }

    public void OnUnityAdsShowFailure(string placementId, UnityAdsShowError error, string message)
    {
        print("interstitial show failure");

    }

    public void OnUnityAdsShowStart(string placementId)
    {
        print("interstitial show start");

    }
}
