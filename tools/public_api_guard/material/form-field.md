## API Report File for "components-srcs"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { _AbstractConstructor } from '@angular/material/core';
import { AfterContentChecked } from '@angular/core';
import { AfterContentInit } from '@angular/core';
import { AfterViewInit } from '@angular/core';
import { AnimationTriggerMetadata } from '@angular/animations';
import { BooleanInput } from '@angular/cdk/coercion';
import { CanColor } from '@angular/material/core';
import { ChangeDetectorRef } from '@angular/core';
import { _Constructor } from '@angular/material/core';
import { Directionality } from '@angular/cdk/bidi';
import { ElementRef } from '@angular/core';
import * as i0 from '@angular/core';
import * as i10 from '@angular/cdk/observers';
import * as i8 from '@angular/common';
import * as i9 from '@angular/material/core';
import { InjectionToken } from '@angular/core';
import { NgControl } from '@angular/forms';
import { NgZone } from '@angular/core';
import { Observable } from 'rxjs';
import { OnDestroy } from '@angular/core';
import { Platform } from '@angular/cdk/platform';
import { QueryList } from '@angular/core';
import { ThemePalette } from '@angular/material/core';

// @public
export type FloatLabelType = 'always' | 'never' | 'auto';

// @public
export function getMatFormFieldDuplicatedHintError(align: string): Error;

// @public
export function getMatFormFieldMissingControlError(): Error;

// @public
export function getMatFormFieldPlaceholderConflictError(): Error;

// @public
export const MAT_ERROR: InjectionToken<MatError>;

// @public
export const MAT_FORM_FIELD: InjectionToken<MatFormField>;

// @public
export const MAT_FORM_FIELD_DEFAULT_OPTIONS: InjectionToken<MatFormFieldDefaultOptions>;

// @public
export const _MAT_HINT: InjectionToken<MatHint>;

// @public
export const MAT_PREFIX: InjectionToken<MatPrefix>;

// @public
export const MAT_SUFFIX: InjectionToken<MatSuffix>;

// @public
export class MatError {
    constructor(ariaLive: string, elementRef: ElementRef);
    // (undocumented)
    id: string;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatError, "mat-error", never, { "id": "id"; }, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatError, [{ attribute: "aria-live"; }, null]>;
}

// @public
export class MatFormField extends _MatFormFieldBase implements AfterContentInit, AfterContentChecked, AfterViewInit, OnDestroy, CanColor {
    constructor(elementRef: ElementRef, _changeDetectorRef: ChangeDetectorRef, _dir: Directionality, _defaults: MatFormFieldDefaultOptions, _platform: Platform, _ngZone: NgZone, _animationMode: string);
    _animateAndLockLabel(): void;
    _animationsEnabled: boolean;
    get appearance(): MatFormFieldAppearance;
    set appearance(value: MatFormFieldAppearance);
    // (undocumented)
    _appearance: MatFormFieldAppearance;
    _canLabelFloat(): boolean;
    // (undocumented)
    _connectionContainerRef: ElementRef;
    // (undocumented)
    get _control(): MatFormFieldControl<any>;
    set _control(value: MatFormFieldControl<any>);
    // (undocumented)
    _controlNonStatic: MatFormFieldControl<any>;
    // (undocumented)
    _controlStatic: MatFormFieldControl<any>;
    // (undocumented)
    _errorChildren: QueryList<MatError>;
    get floatLabel(): FloatLabelType;
    set floatLabel(value: FloatLabelType);
    getConnectedOverlayOrigin(): ElementRef;
    _getDisplayedMessages(): 'error' | 'hint';
    getLabelId(): string | null;
    // (undocumented)
    _hasFloatingLabel(): boolean;
    // (undocumented)
    _hasLabel(): boolean;
    // (undocumented)
    _hasPlaceholder(): boolean;
    // (undocumented)
    _hideControlPlaceholder(): boolean;
    get hideRequiredMarker(): boolean;
    set hideRequiredMarker(value: BooleanInput);
    // (undocumented)
    _hintChildren: QueryList<MatHint>;
    get hintLabel(): string;
    set hintLabel(value: string);
    // (undocumented)
    readonly _hintLabelId: string;
    // (undocumented)
    _inputContainerRef: ElementRef;
    // (undocumented)
    _labelChildNonStatic: MatLabel;
    // (undocumented)
    _labelChildStatic: MatLabel;
    // (undocumented)
    readonly _labelId: string;
    // (undocumented)
    ngAfterContentChecked(): void;
    // (undocumented)
    ngAfterContentInit(): void;
    // (undocumented)
    ngAfterViewInit(): void;
    // (undocumented)
    ngOnDestroy(): void;
    // (undocumented)
    _placeholderChild: MatPlaceholder;
    // (undocumented)
    _prefixChildren: QueryList<MatPrefix>;
    _shouldAlwaysFloat(): boolean;
    _shouldForward(prop: keyof NgControl): boolean;
    // (undocumented)
    _shouldLabelFloat(): boolean;
    _subscriptAnimationState: string;
    // (undocumented)
    _suffixChildren: QueryList<MatSuffix>;
    updateOutlineGap(): void;
    protected _validateControlChild(): void;
    // (undocumented)
    static ɵcmp: i0.ɵɵComponentDeclaration<MatFormField, "mat-form-field", ["matFormField"], { "color": "color"; "appearance": "appearance"; "hideRequiredMarker": "hideRequiredMarker"; "hintLabel": "hintLabel"; "floatLabel": "floatLabel"; }, {}, ["_controlNonStatic", "_controlStatic", "_labelChildNonStatic", "_labelChildStatic", "_placeholderChild", "_errorChildren", "_hintChildren", "_prefixChildren", "_suffixChildren"], ["[matPrefix]", "*", "mat-placeholder", "mat-label", "[matSuffix]", "mat-error", "mat-hint:not([align='end'])", "mat-hint[align='end']"]>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatFormField, [null, null, { optional: true; }, { optional: true; }, null, null, { optional: true; }]>;
}

// @public
export const matFormFieldAnimations: {
    readonly transitionMessages: AnimationTriggerMetadata;
};

// @public
export type MatFormFieldAppearance = 'legacy' | 'standard' | 'fill' | 'outline';

// @public
export abstract class MatFormFieldControl<T> {
    readonly autofilled?: boolean;
    readonly controlType?: string;
    readonly disabled: boolean;
    readonly empty: boolean;
    readonly errorState: boolean;
    readonly focused: boolean;
    readonly id: string;
    readonly ngControl: NgControl | null;
    abstract onContainerClick(event: MouseEvent): void;
    readonly placeholder: string;
    readonly required: boolean;
    abstract setDescribedByIds(ids: string[]): void;
    readonly shouldLabelFloat: boolean;
    readonly stateChanges: Observable<void>;
    readonly userAriaDescribedBy?: string;
    value: T | null;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatFormFieldControl<any>, never, never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatFormFieldControl<any>, never>;
}

// @public
export interface MatFormFieldDefaultOptions {
    appearance?: MatFormFieldAppearance;
    color?: ThemePalette;
    floatLabel?: FloatLabelType;
    hideRequiredMarker?: boolean;
}

// @public (undocumented)
export class MatFormFieldModule {
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatFormFieldModule, never>;
    // (undocumented)
    static ɵinj: i0.ɵɵInjectorDeclaration<MatFormFieldModule>;
    // (undocumented)
    static ɵmod: i0.ɵɵNgModuleDeclaration<MatFormFieldModule, [typeof i1.MatError, typeof i2.MatFormField, typeof i3.MatHint, typeof i4.MatLabel, typeof i5.MatPlaceholder, typeof i6.MatPrefix, typeof i7.MatSuffix], [typeof i8.CommonModule, typeof i9.MatCommonModule, typeof i10.ObserversModule], [typeof i9.MatCommonModule, typeof i1.MatError, typeof i2.MatFormField, typeof i3.MatHint, typeof i4.MatLabel, typeof i5.MatPlaceholder, typeof i6.MatPrefix, typeof i7.MatSuffix]>;
}

// @public
export class MatHint {
    align: 'start' | 'end';
    id: string;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatHint, "mat-hint", never, { "align": "align"; "id": "id"; }, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatHint, never>;
}

// @public
export class MatLabel {
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatLabel, "mat-label", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatLabel, never>;
}

// @public @deprecated
export class MatPlaceholder {
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatPlaceholder, "mat-placeholder", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatPlaceholder, never>;
}

// @public
export class MatPrefix {
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatPrefix, "[matPrefix]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatPrefix, never>;
}

// @public
export class MatSuffix {
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatSuffix, "[matSuffix]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatSuffix, never>;
}

// (No @packageDocumentation comment for this package)

```
